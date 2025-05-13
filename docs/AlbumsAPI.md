# AlbumsAPI

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addAssetsToAlbum**](AlbumsAPI.md#addassetstoalbum) | **PUT** /albums/{id}/assets | 
[**addUsersToAlbum**](AlbumsAPI.md#adduserstoalbum) | **PUT** /albums/{id}/users | 
[**createAlbum**](AlbumsAPI.md#createalbum) | **POST** /albums | 
[**deleteAlbum**](AlbumsAPI.md#deletealbum) | **DELETE** /albums/{id} | 
[**getAlbumInfo**](AlbumsAPI.md#getalbuminfo) | **GET** /albums/{id} | 
[**getAlbumStatistics**](AlbumsAPI.md#getalbumstatistics) | **GET** /albums/statistics | 
[**getAllAlbums**](AlbumsAPI.md#getallalbums) | **GET** /albums | 
[**removeAssetFromAlbum**](AlbumsAPI.md#removeassetfromalbum) | **DELETE** /albums/{id}/assets | 
[**removeUserFromAlbum**](AlbumsAPI.md#removeuserfromalbum) | **DELETE** /albums/{id}/user/{userId} | 
[**updateAlbumInfo**](AlbumsAPI.md#updatealbuminfo) | **PATCH** /albums/{id} | 
[**updateAlbumUser**](AlbumsAPI.md#updatealbumuser) | **PUT** /albums/{id}/user/{userId} | 


# **addAssetsToAlbum**
```swift
    open class func addAssetsToAlbum(id: UUID, bulkIdsDto: BulkIdsDto, key: String? = nil, completion: @escaping (_ data: [BulkIdResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let bulkIdsDto = BulkIdsDto(ids: [123]) // BulkIdsDto | 
let key = "key_example" // String |  (optional)

AlbumsAPI.addAssetsToAlbum(id: id, bulkIdsDto: bulkIdsDto, key: key) { (response, error) in
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
 **key** | **String** |  | [optional] 

### Return type

[**[BulkIdResponseDto]**](BulkIdResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **addUsersToAlbum**
```swift
    open class func addUsersToAlbum(id: UUID, addUsersDto: AddUsersDto, completion: @escaping (_ data: AlbumResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let addUsersDto = AddUsersDto(albumUsers: [AlbumUserAddDto(role: AlbumUserRole(), userId: 123)]) // AddUsersDto | 

AlbumsAPI.addUsersToAlbum(id: id, addUsersDto: addUsersDto) { (response, error) in
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
 **addUsersDto** | [**AddUsersDto**](AddUsersDto.md) |  | 

### Return type

[**AlbumResponseDto**](AlbumResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createAlbum**
```swift
    open class func createAlbum(createAlbumDto: CreateAlbumDto, completion: @escaping (_ data: AlbumResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createAlbumDto = CreateAlbumDto(albumName: "albumName_example", albumUsers: [AlbumUserCreateDto(role: AlbumUserRole(), userId: 123)], assetIds: [123], description: "description_example") // CreateAlbumDto | 

AlbumsAPI.createAlbum(createAlbumDto: createAlbumDto) { (response, error) in
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
 **createAlbumDto** | [**CreateAlbumDto**](CreateAlbumDto.md) |  | 

### Return type

[**AlbumResponseDto**](AlbumResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteAlbum**
```swift
    open class func deleteAlbum(id: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 

AlbumsAPI.deleteAlbum(id: id) { (response, error) in
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

# **getAlbumInfo**
```swift
    open class func getAlbumInfo(id: UUID, key: String? = nil, withoutAssets: Bool? = nil, completion: @escaping (_ data: AlbumResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let key = "key_example" // String |  (optional)
let withoutAssets = true // Bool |  (optional)

AlbumsAPI.getAlbumInfo(id: id, key: key, withoutAssets: withoutAssets) { (response, error) in
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
 **key** | **String** |  | [optional] 
 **withoutAssets** | **Bool** |  | [optional] 

### Return type

[**AlbumResponseDto**](AlbumResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getAlbumStatistics**
```swift
    open class func getAlbumStatistics(completion: @escaping (_ data: AlbumStatisticsResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient


AlbumsAPI.getAlbumStatistics() { (response, error) in
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

[**AlbumStatisticsResponseDto**](AlbumStatisticsResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getAllAlbums**
```swift
    open class func getAllAlbums(assetId: UUID? = nil, shared: Bool? = nil, completion: @escaping (_ data: [AlbumResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let assetId = 987 // UUID | Only returns albums that contain the asset Ignores the shared parameter undefined: get all albums (optional)
let shared = true // Bool |  (optional)

AlbumsAPI.getAllAlbums(assetId: assetId, shared: shared) { (response, error) in
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
 **assetId** | **UUID** | Only returns albums that contain the asset Ignores the shared parameter undefined: get all albums | [optional] 
 **shared** | **Bool** |  | [optional] 

### Return type

[**[AlbumResponseDto]**](AlbumResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **removeAssetFromAlbum**
```swift
    open class func removeAssetFromAlbum(id: UUID, bulkIdsDto: BulkIdsDto, completion: @escaping (_ data: [BulkIdResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let bulkIdsDto = BulkIdsDto(ids: [123]) // BulkIdsDto | 

AlbumsAPI.removeAssetFromAlbum(id: id, bulkIdsDto: bulkIdsDto) { (response, error) in
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

# **removeUserFromAlbum**
```swift
    open class func removeUserFromAlbum(id: UUID, userId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let userId = "userId_example" // String | 

AlbumsAPI.removeUserFromAlbum(id: id, userId: userId) { (response, error) in
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
 **userId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateAlbumInfo**
```swift
    open class func updateAlbumInfo(id: UUID, updateAlbumDto: UpdateAlbumDto, completion: @escaping (_ data: AlbumResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let updateAlbumDto = UpdateAlbumDto(albumName: "albumName_example", albumThumbnailAssetId: 123, description: "description_example", isActivityEnabled: false, order: AssetOrder()) // UpdateAlbumDto | 

AlbumsAPI.updateAlbumInfo(id: id, updateAlbumDto: updateAlbumDto) { (response, error) in
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
 **updateAlbumDto** | [**UpdateAlbumDto**](UpdateAlbumDto.md) |  | 

### Return type

[**AlbumResponseDto**](AlbumResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateAlbumUser**
```swift
    open class func updateAlbumUser(id: UUID, userId: String, updateAlbumUserDto: UpdateAlbumUserDto, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let userId = "userId_example" // String | 
let updateAlbumUserDto = UpdateAlbumUserDto(role: AlbumUserRole()) // UpdateAlbumUserDto | 

AlbumsAPI.updateAlbumUser(id: id, userId: userId, updateAlbumUserDto: updateAlbumUserDto) { (response, error) in
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
 **userId** | **String** |  | 
 **updateAlbumUserDto** | [**UpdateAlbumUserDto**](UpdateAlbumUserDto.md) |  | 

### Return type

Void (empty response body)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

