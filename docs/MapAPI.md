# MapAPI

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getMapMarkers**](MapAPI.md#getmapmarkers) | **GET** /map/markers | 
[**reverseGeocode**](MapAPI.md#reversegeocode) | **GET** /map/reverse-geocode | 


# **getMapMarkers**
```swift
    open class func getMapMarkers(fileCreatedAfter: Date? = nil, fileCreatedBefore: Date? = nil, isArchived: Bool? = nil, isFavorite: Bool? = nil, withPartners: Bool? = nil, withSharedAlbums: Bool? = nil, completion: @escaping (_ data: [MapMarkerResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let fileCreatedAfter = Date() // Date |  (optional)
let fileCreatedBefore = Date() // Date |  (optional)
let isArchived = true // Bool |  (optional)
let isFavorite = true // Bool |  (optional)
let withPartners = true // Bool |  (optional)
let withSharedAlbums = true // Bool |  (optional)

MapAPI.getMapMarkers(fileCreatedAfter: fileCreatedAfter, fileCreatedBefore: fileCreatedBefore, isArchived: isArchived, isFavorite: isFavorite, withPartners: withPartners, withSharedAlbums: withSharedAlbums) { (response, error) in
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
 **fileCreatedAfter** | **Date** |  | [optional] 
 **fileCreatedBefore** | **Date** |  | [optional] 
 **isArchived** | **Bool** |  | [optional] 
 **isFavorite** | **Bool** |  | [optional] 
 **withPartners** | **Bool** |  | [optional] 
 **withSharedAlbums** | **Bool** |  | [optional] 

### Return type

[**[MapMarkerResponseDto]**](MapMarkerResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reverseGeocode**
```swift
    open class func reverseGeocode(lat: Double, lon: Double, completion: @escaping (_ data: [MapReverseGeocodeResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let lat = 987 // Double | 
let lon = 987 // Double | 

MapAPI.reverseGeocode(lat: lat, lon: lon) { (response, error) in
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
 **lat** | **Double** |  | 
 **lon** | **Double** |  | 

### Return type

[**[MapReverseGeocodeResponseDto]**](MapReverseGeocodeResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

