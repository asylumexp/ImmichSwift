# SharedLinksAPI

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addSharedLinkAssets**](SharedLinksAPI.md#addsharedlinkassets) | **PUT** /shared-links/{id}/assets | 
[**createSharedLink**](SharedLinksAPI.md#createsharedlink) | **POST** /shared-links | 
[**getAllSharedLinks**](SharedLinksAPI.md#getallsharedlinks) | **GET** /shared-links | 
[**getMySharedLink**](SharedLinksAPI.md#getmysharedlink) | **GET** /shared-links/me | 
[**getSharedLinkById**](SharedLinksAPI.md#getsharedlinkbyid) | **GET** /shared-links/{id} | 
[**removeSharedLink**](SharedLinksAPI.md#removesharedlink) | **DELETE** /shared-links/{id} | 
[**removeSharedLinkAssets**](SharedLinksAPI.md#removesharedlinkassets) | **DELETE** /shared-links/{id}/assets | 
[**updateSharedLink**](SharedLinksAPI.md#updatesharedlink) | **PATCH** /shared-links/{id} | 


# **addSharedLinkAssets**
```swift
    open class func addSharedLinkAssets(id: UUID, assetIdsDto: AssetIdsDto, key: String? = nil, completion: @escaping (_ data: [AssetIdsResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let assetIdsDto = AssetIdsDto(assetIds: [123]) // AssetIdsDto | 
let key = "key_example" // String |  (optional)

SharedLinksAPI.addSharedLinkAssets(id: id, assetIdsDto: assetIdsDto, key: key) { (response, error) in
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
 **assetIdsDto** | [**AssetIdsDto**](AssetIdsDto.md) |  | 
 **key** | **String** |  | [optional] 

### Return type

[**[AssetIdsResponseDto]**](AssetIdsResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createSharedLink**
```swift
    open class func createSharedLink(sharedLinkCreateDto: SharedLinkCreateDto, completion: @escaping (_ data: SharedLinkResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let sharedLinkCreateDto = SharedLinkCreateDto(albumId: 123, allowDownload: false, allowUpload: false, assetIds: [123], description: "description_example", expiresAt: Date(), password: "password_example", showMetadata: false, type: SharedLinkType()) // SharedLinkCreateDto | 

SharedLinksAPI.createSharedLink(sharedLinkCreateDto: sharedLinkCreateDto) { (response, error) in
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
 **sharedLinkCreateDto** | [**SharedLinkCreateDto**](SharedLinkCreateDto.md) |  | 

### Return type

[**SharedLinkResponseDto**](SharedLinkResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getAllSharedLinks**
```swift
    open class func getAllSharedLinks(albumId: UUID? = nil, completion: @escaping (_ data: [SharedLinkResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let albumId = 987 // UUID |  (optional)

SharedLinksAPI.getAllSharedLinks(albumId: albumId) { (response, error) in
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
 **albumId** | **UUID** |  | [optional] 

### Return type

[**[SharedLinkResponseDto]**](SharedLinkResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getMySharedLink**
```swift
    open class func getMySharedLink(key: String? = nil, password: String? = nil, token: String? = nil, completion: @escaping (_ data: SharedLinkResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let key = "key_example" // String |  (optional)
let password = "password_example" // String |  (optional)
let token = "token_example" // String |  (optional)

SharedLinksAPI.getMySharedLink(key: key, password: password, token: token) { (response, error) in
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
 **key** | **String** |  | [optional] 
 **password** | **String** |  | [optional] 
 **token** | **String** |  | [optional] 

### Return type

[**SharedLinkResponseDto**](SharedLinkResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getSharedLinkById**
```swift
    open class func getSharedLinkById(id: UUID, completion: @escaping (_ data: SharedLinkResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 

SharedLinksAPI.getSharedLinkById(id: id) { (response, error) in
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

[**SharedLinkResponseDto**](SharedLinkResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **removeSharedLink**
```swift
    open class func removeSharedLink(id: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 

SharedLinksAPI.removeSharedLink(id: id) { (response, error) in
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

# **removeSharedLinkAssets**
```swift
    open class func removeSharedLinkAssets(id: UUID, assetIdsDto: AssetIdsDto, key: String? = nil, completion: @escaping (_ data: [AssetIdsResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let assetIdsDto = AssetIdsDto(assetIds: [123]) // AssetIdsDto | 
let key = "key_example" // String |  (optional)

SharedLinksAPI.removeSharedLinkAssets(id: id, assetIdsDto: assetIdsDto, key: key) { (response, error) in
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
 **assetIdsDto** | [**AssetIdsDto**](AssetIdsDto.md) |  | 
 **key** | **String** |  | [optional] 

### Return type

[**[AssetIdsResponseDto]**](AssetIdsResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateSharedLink**
```swift
    open class func updateSharedLink(id: UUID, sharedLinkEditDto: SharedLinkEditDto, completion: @escaping (_ data: SharedLinkResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let sharedLinkEditDto = SharedLinkEditDto(allowDownload: false, allowUpload: false, changeExpiryTime: false, description: "description_example", expiresAt: Date(), password: "password_example", showMetadata: false) // SharedLinkEditDto | 

SharedLinksAPI.updateSharedLink(id: id, sharedLinkEditDto: sharedLinkEditDto) { (response, error) in
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
 **sharedLinkEditDto** | [**SharedLinkEditDto**](SharedLinkEditDto.md) |  | 

### Return type

[**SharedLinkResponseDto**](SharedLinkResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

