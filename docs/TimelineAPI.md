# TimelineAPI

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getTimeBucket**](TimelineAPI.md#gettimebucket) | **GET** /timeline/bucket | 
[**getTimeBuckets**](TimelineAPI.md#gettimebuckets) | **GET** /timeline/buckets | 


# **getTimeBucket**
```swift
    open class func getTimeBucket(size: TimeBucketSize, timeBucket: String, albumId: UUID? = nil, isFavorite: Bool? = nil, isTrashed: Bool? = nil, key: String? = nil, order: AssetOrder? = nil, personId: UUID? = nil, tagId: UUID? = nil, userId: UUID? = nil, visibility: AssetVisibility? = nil, withPartners: Bool? = nil, withStacked: Bool? = nil, completion: @escaping (_ data: [AssetResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let size = TimeBucketSize() // TimeBucketSize | 
let timeBucket = "timeBucket_example" // String | 
let albumId = 987 // UUID |  (optional)
let isFavorite = true // Bool |  (optional)
let isTrashed = true // Bool |  (optional)
let key = "key_example" // String |  (optional)
let order = AssetOrder() // AssetOrder |  (optional)
let personId = 987 // UUID |  (optional)
let tagId = 987 // UUID |  (optional)
let userId = 987 // UUID |  (optional)
let visibility = AssetVisibility() // AssetVisibility |  (optional)
let withPartners = true // Bool |  (optional)
let withStacked = true // Bool |  (optional)

TimelineAPI.getTimeBucket(size: size, timeBucket: timeBucket, albumId: albumId, isFavorite: isFavorite, isTrashed: isTrashed, key: key, order: order, personId: personId, tagId: tagId, userId: userId, visibility: visibility, withPartners: withPartners, withStacked: withStacked) { (response, error) in
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
 **size** | [**TimeBucketSize**](.md) |  | 
 **timeBucket** | **String** |  | 
 **albumId** | **UUID** |  | [optional] 
 **isFavorite** | **Bool** |  | [optional] 
 **isTrashed** | **Bool** |  | [optional] 
 **key** | **String** |  | [optional] 
 **order** | [**AssetOrder**](.md) |  | [optional] 
 **personId** | **UUID** |  | [optional] 
 **tagId** | **UUID** |  | [optional] 
 **userId** | **UUID** |  | [optional] 
 **visibility** | [**AssetVisibility**](.md) |  | [optional] 
 **withPartners** | **Bool** |  | [optional] 
 **withStacked** | **Bool** |  | [optional] 

### Return type

[**[AssetResponseDto]**](AssetResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getTimeBuckets**
```swift
    open class func getTimeBuckets(size: TimeBucketSize, albumId: UUID? = nil, isFavorite: Bool? = nil, isTrashed: Bool? = nil, key: String? = nil, order: AssetOrder? = nil, personId: UUID? = nil, tagId: UUID? = nil, userId: UUID? = nil, visibility: AssetVisibility? = nil, withPartners: Bool? = nil, withStacked: Bool? = nil, completion: @escaping (_ data: [TimeBucketResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let size = TimeBucketSize() // TimeBucketSize | 
let albumId = 987 // UUID |  (optional)
let isFavorite = true // Bool |  (optional)
let isTrashed = true // Bool |  (optional)
let key = "key_example" // String |  (optional)
let order = AssetOrder() // AssetOrder |  (optional)
let personId = 987 // UUID |  (optional)
let tagId = 987 // UUID |  (optional)
let userId = 987 // UUID |  (optional)
let visibility = AssetVisibility() // AssetVisibility |  (optional)
let withPartners = true // Bool |  (optional)
let withStacked = true // Bool |  (optional)

TimelineAPI.getTimeBuckets(size: size, albumId: albumId, isFavorite: isFavorite, isTrashed: isTrashed, key: key, order: order, personId: personId, tagId: tagId, userId: userId, visibility: visibility, withPartners: withPartners, withStacked: withStacked) { (response, error) in
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
 **size** | [**TimeBucketSize**](.md) |  | 
 **albumId** | **UUID** |  | [optional] 
 **isFavorite** | **Bool** |  | [optional] 
 **isTrashed** | **Bool** |  | [optional] 
 **key** | **String** |  | [optional] 
 **order** | [**AssetOrder**](.md) |  | [optional] 
 **personId** | **UUID** |  | [optional] 
 **tagId** | **UUID** |  | [optional] 
 **userId** | **UUID** |  | [optional] 
 **visibility** | [**AssetVisibility**](.md) |  | [optional] 
 **withPartners** | **Bool** |  | [optional] 
 **withStacked** | **Bool** |  | [optional] 

### Return type

[**[TimeBucketResponseDto]**](TimeBucketResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

