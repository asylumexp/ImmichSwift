# SyncAPI

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteSyncAck**](SyncAPI.md#deletesyncack) | **DELETE** /sync/ack | 
[**getDeltaSync**](SyncAPI.md#getdeltasync) | **POST** /sync/delta-sync | 
[**getFullSyncForUser**](SyncAPI.md#getfullsyncforuser) | **POST** /sync/full-sync | 
[**getSyncAck**](SyncAPI.md#getsyncack) | **GET** /sync/ack | 
[**getSyncStream**](SyncAPI.md#getsyncstream) | **POST** /sync/stream | 
[**sendSyncAck**](SyncAPI.md#sendsyncack) | **POST** /sync/ack | 


# **deleteSyncAck**
```swift
    open class func deleteSyncAck(syncAckDeleteDto: SyncAckDeleteDto, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let syncAckDeleteDto = SyncAckDeleteDto(types: [SyncEntityType()]) // SyncAckDeleteDto | 

SyncAPI.deleteSyncAck(syncAckDeleteDto: syncAckDeleteDto) { (response, error) in
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
 **syncAckDeleteDto** | [**SyncAckDeleteDto**](SyncAckDeleteDto.md) |  | 

### Return type

Void (empty response body)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getDeltaSync**
```swift
    open class func getDeltaSync(assetDeltaSyncDto: AssetDeltaSyncDto, completion: @escaping (_ data: AssetDeltaSyncResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let assetDeltaSyncDto = AssetDeltaSyncDto(updatedAfter: Date(), userIds: [123]) // AssetDeltaSyncDto | 

SyncAPI.getDeltaSync(assetDeltaSyncDto: assetDeltaSyncDto) { (response, error) in
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
 **assetDeltaSyncDto** | [**AssetDeltaSyncDto**](AssetDeltaSyncDto.md) |  | 

### Return type

[**AssetDeltaSyncResponseDto**](AssetDeltaSyncResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getFullSyncForUser**
```swift
    open class func getFullSyncForUser(assetFullSyncDto: AssetFullSyncDto, completion: @escaping (_ data: [AssetResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let assetFullSyncDto = AssetFullSyncDto(lastId: 123, limit: 123, updatedUntil: Date(), userId: 123) // AssetFullSyncDto | 

SyncAPI.getFullSyncForUser(assetFullSyncDto: assetFullSyncDto) { (response, error) in
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
 **assetFullSyncDto** | [**AssetFullSyncDto**](AssetFullSyncDto.md) |  | 

### Return type

[**[AssetResponseDto]**](AssetResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getSyncAck**
```swift
    open class func getSyncAck(completion: @escaping (_ data: [SyncAckDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient


SyncAPI.getSyncAck() { (response, error) in
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
This endpoint does not need any parameter.

### Return type

[**[SyncAckDto]**](SyncAckDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getSyncStream**
```swift
    open class func getSyncStream(syncStreamDto: SyncStreamDto, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let syncStreamDto = SyncStreamDto(types: [SyncRequestType()]) // SyncStreamDto | 

SyncAPI.getSyncStream(syncStreamDto: syncStreamDto) { (response, error) in
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
 **syncStreamDto** | [**SyncStreamDto**](SyncStreamDto.md) |  | 

### Return type

Void (empty response body)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **sendSyncAck**
```swift
    open class func sendSyncAck(syncAckSetDto: SyncAckSetDto, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let syncAckSetDto = SyncAckSetDto(acks: ["acks_example"]) // SyncAckSetDto | 

SyncAPI.sendSyncAck(syncAckSetDto: syncAckSetDto) { (response, error) in
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
 **syncAckSetDto** | [**SyncAckSetDto**](SyncAckSetDto.md) |  | 

### Return type

Void (empty response body)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

