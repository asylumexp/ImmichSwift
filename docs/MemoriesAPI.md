# MemoriesAPI

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addMemoryAssets**](MemoriesAPI.md#addmemoryassets) | **PUT** /memories/{id}/assets | 
[**createMemory**](MemoriesAPI.md#creatememory) | **POST** /memories | 
[**deleteMemory**](MemoriesAPI.md#deletememory) | **DELETE** /memories/{id} | 
[**getMemory**](MemoriesAPI.md#getmemory) | **GET** /memories/{id} | 
[**removeMemoryAssets**](MemoriesAPI.md#removememoryassets) | **DELETE** /memories/{id}/assets | 
[**searchMemories**](MemoriesAPI.md#searchmemories) | **GET** /memories | 
[**updateMemory**](MemoriesAPI.md#updatememory) | **PUT** /memories/{id} | 


# **addMemoryAssets**
```swift
    open class func addMemoryAssets(id: UUID, bulkIdsDto: BulkIdsDto, completion: @escaping (_ data: [BulkIdResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let bulkIdsDto = BulkIdsDto(ids: [123]) // BulkIdsDto | 

MemoriesAPI.addMemoryAssets(id: id, bulkIdsDto: bulkIdsDto) { (response, error) in
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
 **bulkIdsDto** | [**BulkIdsDto**](BulkIdsDto.md) |  | 

### Return type

[**[BulkIdResponseDto]**](BulkIdResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createMemory**
```swift
    open class func createMemory(memoryCreateDto: MemoryCreateDto, completion: @escaping (_ data: MemoryResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let memoryCreateDto = MemoryCreateDto(assetIds: [123], data: OnThisDayDto(year: 123), isSaved: false, memoryAt: Date(), seenAt: Date(), type: MemoryType()) // MemoryCreateDto | 

MemoriesAPI.createMemory(memoryCreateDto: memoryCreateDto) { (response, error) in
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
 **memoryCreateDto** | [**MemoryCreateDto**](MemoryCreateDto.md) |  | 

### Return type

[**MemoryResponseDto**](MemoryResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteMemory**
```swift
    open class func deleteMemory(id: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 

MemoriesAPI.deleteMemory(id: id) { (response, error) in
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

# **getMemory**
```swift
    open class func getMemory(id: UUID, completion: @escaping (_ data: MemoryResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 

MemoriesAPI.getMemory(id: id) { (response, error) in
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

[**MemoryResponseDto**](MemoryResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **removeMemoryAssets**
```swift
    open class func removeMemoryAssets(id: UUID, bulkIdsDto: BulkIdsDto, completion: @escaping (_ data: [BulkIdResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let bulkIdsDto = BulkIdsDto(ids: [123]) // BulkIdsDto | 

MemoriesAPI.removeMemoryAssets(id: id, bulkIdsDto: bulkIdsDto) { (response, error) in
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
 **bulkIdsDto** | [**BulkIdsDto**](BulkIdsDto.md) |  | 

### Return type

[**[BulkIdResponseDto]**](BulkIdResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **searchMemories**
```swift
    open class func searchMemories(_for: Date? = nil, isSaved: Bool? = nil, isTrashed: Bool? = nil, type: MemoryType? = nil, completion: @escaping (_ data: [MemoryResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let _for = Date() // Date |  (optional)
let isSaved = true // Bool |  (optional)
let isTrashed = true // Bool |  (optional)
let type = MemoryType() // MemoryType |  (optional)

MemoriesAPI.searchMemories(_for: _for, isSaved: isSaved, isTrashed: isTrashed, type: type) { (response, error) in
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
 **_for** | **Date** |  | [optional] 
 **isSaved** | **Bool** |  | [optional] 
 **isTrashed** | **Bool** |  | [optional] 
 **type** | [**MemoryType**](.md) |  | [optional] 

### Return type

[**[MemoryResponseDto]**](MemoryResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateMemory**
```swift
    open class func updateMemory(id: UUID, memoryUpdateDto: MemoryUpdateDto, completion: @escaping (_ data: MemoryResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let memoryUpdateDto = MemoryUpdateDto(isSaved: false, memoryAt: Date(), seenAt: Date()) // MemoryUpdateDto | 

MemoriesAPI.updateMemory(id: id, memoryUpdateDto: memoryUpdateDto) { (response, error) in
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
 **memoryUpdateDto** | [**MemoryUpdateDto**](MemoryUpdateDto.md) |  | 

### Return type

[**MemoryResponseDto**](MemoryResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

