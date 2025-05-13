# ActivitiesAPI

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createActivity**](ActivitiesAPI.md#createactivity) | **POST** /activities | 
[**deleteActivity**](ActivitiesAPI.md#deleteactivity) | **DELETE** /activities/{id} | 
[**getActivities**](ActivitiesAPI.md#getactivities) | **GET** /activities | 
[**getActivityStatistics**](ActivitiesAPI.md#getactivitystatistics) | **GET** /activities/statistics | 


# **createActivity**
```swift
    open class func createActivity(activityCreateDto: ActivityCreateDto, completion: @escaping (_ data: ActivityResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let activityCreateDto = ActivityCreateDto(albumId: 123, assetId: 123, comment: "comment_example", type: ReactionType()) // ActivityCreateDto | 

ActivitiesAPI.createActivity(activityCreateDto: activityCreateDto) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **activityCreateDto** | [**ActivityCreateDto**](ActivityCreateDto.md) |  | 

### Return type

[**ActivityResponseDto**](ActivityResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteActivity**
```swift
    open class func deleteActivity(id: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 

ActivitiesAPI.deleteActivity(id: id) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **UUID** |  | 

### Return type

Void (empty response body)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getActivities**
```swift
    open class func getActivities(albumId: UUID, assetId: UUID? = nil, level: ReactionLevel? = nil, type: ReactionType? = nil, userId: UUID? = nil, completion: @escaping (_ data: [ActivityResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let albumId = 987 // UUID | 
let assetId = 987 // UUID |  (optional)
let level = ReactionLevel() // ReactionLevel |  (optional)
let type = ReactionType() // ReactionType |  (optional)
let userId = 987 // UUID |  (optional)

ActivitiesAPI.getActivities(albumId: albumId, assetId: assetId, level: level, type: type, userId: userId) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **albumId** | **UUID** |  | 
 **assetId** | **UUID** |  | [optional] 
 **level** | [**ReactionLevel**](.md) |  | [optional] 
 **type** | [**ReactionType**](.md) |  | [optional] 
 **userId** | **UUID** |  | [optional] 

### Return type

[**[ActivityResponseDto]**](ActivityResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getActivityStatistics**
```swift
    open class func getActivityStatistics(albumId: UUID, assetId: UUID? = nil, completion: @escaping (_ data: ActivityStatisticsResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let albumId = 987 // UUID | 
let assetId = 987 // UUID |  (optional)

ActivitiesAPI.getActivityStatistics(albumId: albumId, assetId: assetId) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **albumId** | **UUID** |  | 
 **assetId** | **UUID** |  | [optional] 

### Return type

[**ActivityStatisticsResponseDto**](ActivityStatisticsResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

