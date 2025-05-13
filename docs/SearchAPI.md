# SearchAPI

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getAssetsByCity**](SearchAPI.md#getassetsbycity) | **GET** /search/cities | 
[**getExploreData**](SearchAPI.md#getexploredata) | **GET** /search/explore | 
[**getSearchSuggestions**](SearchAPI.md#getsearchsuggestions) | **GET** /search/suggestions | 
[**searchAssets**](SearchAPI.md#searchassets) | **POST** /search/metadata | 
[**searchPerson**](SearchAPI.md#searchperson) | **GET** /search/person | 
[**searchPlaces**](SearchAPI.md#searchplaces) | **GET** /search/places | 
[**searchRandom**](SearchAPI.md#searchrandom) | **POST** /search/random | 
[**searchSmart**](SearchAPI.md#searchsmart) | **POST** /search/smart | 


# **getAssetsByCity**
```swift
    open class func getAssetsByCity(completion: @escaping (_ data: [AssetResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient


SearchAPI.getAssetsByCity() { (response, error) in
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

[**[AssetResponseDto]**](AssetResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getExploreData**
```swift
    open class func getExploreData(completion: @escaping (_ data: [SearchExploreResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient


SearchAPI.getExploreData() { (response, error) in
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

[**[SearchExploreResponseDto]**](SearchExploreResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getSearchSuggestions**
```swift
    open class func getSearchSuggestions(type: SearchSuggestionType, country: String? = nil, includeNull: Bool? = nil, make: String? = nil, model: String? = nil, state: String? = nil, completion: @escaping (_ data: [String]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let type = SearchSuggestionType() // SearchSuggestionType | 
let country = "country_example" // String |  (optional)
let includeNull = true // Bool | This property was added in v111.0.0 (optional)
let make = "make_example" // String |  (optional)
let model = "model_example" // String |  (optional)
let state = "state_example" // String |  (optional)

SearchAPI.getSearchSuggestions(type: type, country: country, includeNull: includeNull, make: make, model: model, state: state) { (response, error) in
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
 **type** | [**SearchSuggestionType**](.md) |  | 
 **country** | **String** |  | [optional] 
 **includeNull** | **Bool** | This property was added in v111.0.0 | [optional] 
 **make** | **String** |  | [optional] 
 **model** | **String** |  | [optional] 
 **state** | **String** |  | [optional] 

### Return type

**[String]**

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **searchAssets**
```swift
    open class func searchAssets(metadataSearchDto: MetadataSearchDto, completion: @escaping (_ data: SearchResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let metadataSearchDto = MetadataSearchDto(checksum: "checksum_example", city: "city_example", country: "country_example", createdAfter: Date(), createdBefore: Date(), description: "description_example", deviceAssetId: "deviceAssetId_example", deviceId: "deviceId_example", encodedVideoPath: "encodedVideoPath_example", id: 123, isEncoded: false, isFavorite: false, isMotion: false, isNotInAlbum: false, isOffline: false, lensModel: "lensModel_example", libraryId: 123, make: "make_example", model: "model_example", order: AssetOrder(), originalFileName: "originalFileName_example", originalPath: "originalPath_example", page: 123, personIds: [123], previewPath: "previewPath_example", rating: 123, size: 123, state: "state_example", tagIds: [123], takenAfter: Date(), takenBefore: Date(), thumbnailPath: "thumbnailPath_example", trashedAfter: Date(), trashedBefore: Date(), type: AssetTypeEnum(), updatedAfter: Date(), updatedBefore: Date(), visibility: AssetVisibility(), withDeleted: false, withExif: false, withPeople: false, withStacked: false) // MetadataSearchDto | 

SearchAPI.searchAssets(metadataSearchDto: metadataSearchDto) { (response, error) in
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
 **metadataSearchDto** | [**MetadataSearchDto**](MetadataSearchDto.md) |  | 

### Return type

[**SearchResponseDto**](SearchResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **searchPerson**
```swift
    open class func searchPerson(name: String, withHidden: Bool? = nil, completion: @escaping (_ data: [PersonResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let name = "name_example" // String | 
let withHidden = true // Bool |  (optional)

SearchAPI.searchPerson(name: name, withHidden: withHidden) { (response, error) in
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
 **name** | **String** |  | 
 **withHidden** | **Bool** |  | [optional] 

### Return type

[**[PersonResponseDto]**](PersonResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **searchPlaces**
```swift
    open class func searchPlaces(name: String, completion: @escaping (_ data: [PlacesResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let name = "name_example" // String | 

SearchAPI.searchPlaces(name: name) { (response, error) in
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
 **name** | **String** |  | 

### Return type

[**[PlacesResponseDto]**](PlacesResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **searchRandom**
```swift
    open class func searchRandom(randomSearchDto: RandomSearchDto, completion: @escaping (_ data: [AssetResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let randomSearchDto = RandomSearchDto(city: "city_example", country: "country_example", createdAfter: Date(), createdBefore: Date(), deviceId: "deviceId_example", isEncoded: false, isFavorite: false, isMotion: false, isNotInAlbum: false, isOffline: false, lensModel: "lensModel_example", libraryId: 123, make: "make_example", model: "model_example", personIds: [123], rating: 123, size: 123, state: "state_example", tagIds: [123], takenAfter: Date(), takenBefore: Date(), trashedAfter: Date(), trashedBefore: Date(), type: AssetTypeEnum(), updatedAfter: Date(), updatedBefore: Date(), visibility: AssetVisibility(), withDeleted: false, withExif: false, withPeople: false, withStacked: false) // RandomSearchDto | 

SearchAPI.searchRandom(randomSearchDto: randomSearchDto) { (response, error) in
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
 **randomSearchDto** | [**RandomSearchDto**](RandomSearchDto.md) |  | 

### Return type

[**[AssetResponseDto]**](AssetResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **searchSmart**
```swift
    open class func searchSmart(smartSearchDto: SmartSearchDto, completion: @escaping (_ data: SearchResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let smartSearchDto = SmartSearchDto(city: "city_example", country: "country_example", createdAfter: Date(), createdBefore: Date(), deviceId: "deviceId_example", isEncoded: false, isFavorite: false, isMotion: false, isNotInAlbum: false, isOffline: false, language: "language_example", lensModel: "lensModel_example", libraryId: 123, make: "make_example", model: "model_example", page: 123, personIds: [123], query: "query_example", rating: 123, size: 123, state: "state_example", tagIds: [123], takenAfter: Date(), takenBefore: Date(), trashedAfter: Date(), trashedBefore: Date(), type: AssetTypeEnum(), updatedAfter: Date(), updatedBefore: Date(), visibility: AssetVisibility(), withDeleted: false, withExif: false) // SmartSearchDto | 

SearchAPI.searchSmart(smartSearchDto: smartSearchDto) { (response, error) in
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
 **smartSearchDto** | [**SmartSearchDto**](SmartSearchDto.md) |  | 

### Return type

[**SearchResponseDto**](SearchResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

