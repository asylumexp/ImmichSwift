# FacesAPI

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createFace**](FacesAPI.md#createface) | **POST** /faces | 
[**deleteFace**](FacesAPI.md#deleteface) | **DELETE** /faces/{id} | 
[**getFaces**](FacesAPI.md#getfaces) | **GET** /faces | 
[**reassignFacesById**](FacesAPI.md#reassignfacesbyid) | **PUT** /faces/{id} | 


# **createFace**
```swift
    open class func createFace(assetFaceCreateDto: AssetFaceCreateDto, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let assetFaceCreateDto = AssetFaceCreateDto(assetId: 123, height: 123, imageHeight: 123, imageWidth: 123, personId: 123, width: 123, x: 123, y: 123) // AssetFaceCreateDto | 

FacesAPI.createFace(assetFaceCreateDto: assetFaceCreateDto) { (response, error) in
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
 **assetFaceCreateDto** | [**AssetFaceCreateDto**](AssetFaceCreateDto.md) |  | 

### Return type

Void (empty response body)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteFace**
```swift
    open class func deleteFace(id: UUID, assetFaceDeleteDto: AssetFaceDeleteDto, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let assetFaceDeleteDto = AssetFaceDeleteDto(force: false) // AssetFaceDeleteDto | 

FacesAPI.deleteFace(id: id, assetFaceDeleteDto: assetFaceDeleteDto) { (response, error) in
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
 **assetFaceDeleteDto** | [**AssetFaceDeleteDto**](AssetFaceDeleteDto.md) |  | 

### Return type

Void (empty response body)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getFaces**
```swift
    open class func getFaces(id: UUID, completion: @escaping (_ data: [AssetFaceResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 

FacesAPI.getFaces(id: id) { (response, error) in
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

[**[AssetFaceResponseDto]**](AssetFaceResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reassignFacesById**
```swift
    open class func reassignFacesById(id: UUID, faceDto: FaceDto, completion: @escaping (_ data: PersonResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let faceDto = FaceDto(id: 123) // FaceDto | 

FacesAPI.reassignFacesById(id: id, faceDto: faceDto) { (response, error) in
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
 **faceDto** | [**FaceDto**](FaceDto.md) |  | 

### Return type

[**PersonResponseDto**](PersonResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

