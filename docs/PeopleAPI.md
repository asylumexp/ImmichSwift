# PeopleAPI

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createPerson**](PeopleAPI.md#createperson) | **POST** /people | 
[**getAllPeople**](PeopleAPI.md#getallpeople) | **GET** /people | 
[**getPerson**](PeopleAPI.md#getperson) | **GET** /people/{id} | 
[**getPersonStatistics**](PeopleAPI.md#getpersonstatistics) | **GET** /people/{id}/statistics | 
[**getPersonThumbnail**](PeopleAPI.md#getpersonthumbnail) | **GET** /people/{id}/thumbnail | 
[**mergePerson**](PeopleAPI.md#mergeperson) | **POST** /people/{id}/merge | 
[**reassignFaces**](PeopleAPI.md#reassignfaces) | **PUT** /people/{id}/reassign | 
[**updatePeople**](PeopleAPI.md#updatepeople) | **PUT** /people | 
[**updatePerson**](PeopleAPI.md#updateperson) | **PUT** /people/{id} | 


# **createPerson**
```swift
    open class func createPerson(personCreateDto: PersonCreateDto, completion: @escaping (_ data: PersonResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let personCreateDto = PersonCreateDto(birthDate: Date(), color: "color_example", isFavorite: false, isHidden: false, name: "name_example") // PersonCreateDto | 

PeopleAPI.createPerson(personCreateDto: personCreateDto) { (response, error) in
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
 **personCreateDto** | [**PersonCreateDto**](PersonCreateDto.md) |  | 

### Return type

[**PersonResponseDto**](PersonResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getAllPeople**
```swift
    open class func getAllPeople(closestAssetId: UUID? = nil, closestPersonId: UUID? = nil, page: Double? = nil, size: Double? = nil, withHidden: Bool? = nil, completion: @escaping (_ data: PeopleResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let closestAssetId = 987 // UUID |  (optional)
let closestPersonId = 987 // UUID |  (optional)
let page = 987 // Double | Page number for pagination (optional) (default to 1)
let size = 987 // Double | Number of items per page (optional) (default to 500)
let withHidden = true // Bool |  (optional)

PeopleAPI.getAllPeople(closestAssetId: closestAssetId, closestPersonId: closestPersonId, page: page, size: size, withHidden: withHidden) { (response, error) in
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
 **closestAssetId** | **UUID** |  | [optional] 
 **closestPersonId** | **UUID** |  | [optional] 
 **page** | **Double** | Page number for pagination | [optional] [default to 1]
 **size** | **Double** | Number of items per page | [optional] [default to 500]
 **withHidden** | **Bool** |  | [optional] 

### Return type

[**PeopleResponseDto**](PeopleResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getPerson**
```swift
    open class func getPerson(id: UUID, completion: @escaping (_ data: PersonResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 

PeopleAPI.getPerson(id: id) { (response, error) in
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

[**PersonResponseDto**](PersonResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getPersonStatistics**
```swift
    open class func getPersonStatistics(id: UUID, completion: @escaping (_ data: PersonStatisticsResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 

PeopleAPI.getPersonStatistics(id: id) { (response, error) in
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

[**PersonStatisticsResponseDto**](PersonStatisticsResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getPersonThumbnail**
```swift
    open class func getPersonThumbnail(id: UUID, completion: @escaping (_ data: URL?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 

PeopleAPI.getPersonThumbnail(id: id) { (response, error) in
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

**URL**

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **mergePerson**
```swift
    open class func mergePerson(id: UUID, mergePersonDto: MergePersonDto, completion: @escaping (_ data: [BulkIdResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let mergePersonDto = MergePersonDto(ids: [123]) // MergePersonDto | 

PeopleAPI.mergePerson(id: id, mergePersonDto: mergePersonDto) { (response, error) in
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
 **mergePersonDto** | [**MergePersonDto**](MergePersonDto.md) |  | 

### Return type

[**[BulkIdResponseDto]**](BulkIdResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reassignFaces**
```swift
    open class func reassignFaces(id: UUID, assetFaceUpdateDto: AssetFaceUpdateDto, completion: @escaping (_ data: [PersonResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let assetFaceUpdateDto = AssetFaceUpdateDto(data: [AssetFaceUpdateItem(assetId: 123, personId: 123)]) // AssetFaceUpdateDto | 

PeopleAPI.reassignFaces(id: id, assetFaceUpdateDto: assetFaceUpdateDto) { (response, error) in
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
 **assetFaceUpdateDto** | [**AssetFaceUpdateDto**](AssetFaceUpdateDto.md) |  | 

### Return type

[**[PersonResponseDto]**](PersonResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updatePeople**
```swift
    open class func updatePeople(peopleUpdateDto: PeopleUpdateDto, completion: @escaping (_ data: [BulkIdResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let peopleUpdateDto = PeopleUpdateDto(people: [PeopleUpdateItem(birthDate: Date(), color: "color_example", featureFaceAssetId: "featureFaceAssetId_example", id: "id_example", isFavorite: false, isHidden: false, name: "name_example")]) // PeopleUpdateDto | 

PeopleAPI.updatePeople(peopleUpdateDto: peopleUpdateDto) { (response, error) in
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
 **peopleUpdateDto** | [**PeopleUpdateDto**](PeopleUpdateDto.md) |  | 

### Return type

[**[BulkIdResponseDto]**](BulkIdResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updatePerson**
```swift
    open class func updatePerson(id: UUID, personUpdateDto: PersonUpdateDto, completion: @escaping (_ data: PersonResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let personUpdateDto = PersonUpdateDto(birthDate: Date(), color: "color_example", featureFaceAssetId: "featureFaceAssetId_example", isFavorite: false, isHidden: false, name: "name_example") // PersonUpdateDto | 

PeopleAPI.updatePerson(id: id, personUpdateDto: personUpdateDto) { (response, error) in
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
 **personUpdateDto** | [**PersonUpdateDto**](PersonUpdateDto.md) |  | 

### Return type

[**PersonResponseDto**](PersonResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

