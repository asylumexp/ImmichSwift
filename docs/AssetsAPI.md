# AssetsAPI

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**checkBulkUpload**](AssetsAPI.md#checkbulkupload) | **POST** /assets/bulk-upload-check | checkBulkUpload
[**checkExistingAssets**](AssetsAPI.md#checkexistingassets) | **POST** /assets/exist | checkExistingAssets
[**deleteAssets**](AssetsAPI.md#deleteassets) | **DELETE** /assets | 
[**downloadAsset**](AssetsAPI.md#downloadasset) | **GET** /assets/{id}/original | 
[**getAllUserAssetsByDeviceId**](AssetsAPI.md#getalluserassetsbydeviceid) | **GET** /assets/device/{deviceId} | getAllUserAssetsByDeviceId
[**getAssetInfo**](AssetsAPI.md#getassetinfo) | **GET** /assets/{id} | 
[**getAssetStatistics**](AssetsAPI.md#getassetstatistics) | **GET** /assets/statistics | 
[**getRandom**](AssetsAPI.md#getrandom) | **GET** /assets/random | 
[**playAssetVideo**](AssetsAPI.md#playassetvideo) | **GET** /assets/{id}/video/playback | 
[**replaceAsset**](AssetsAPI.md#replaceasset) | **PUT** /assets/{id}/original | replaceAsset
[**runAssetJobs**](AssetsAPI.md#runassetjobs) | **POST** /assets/jobs | 
[**updateAsset**](AssetsAPI.md#updateasset) | **PUT** /assets/{id} | 
[**updateAssets**](AssetsAPI.md#updateassets) | **PUT** /assets | 
[**uploadAsset**](AssetsAPI.md#uploadasset) | **POST** /assets | 
[**viewAsset**](AssetsAPI.md#viewasset) | **GET** /assets/{id}/thumbnail | 


# **checkBulkUpload**
```swift
    open class func checkBulkUpload(assetBulkUploadCheckDto: AssetBulkUploadCheckDto, completion: @escaping (_ data: AssetBulkUploadCheckResponseDto?, _ error: Error?) -> Void)
```

checkBulkUpload

Checks if assets exist by checksums

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let assetBulkUploadCheckDto = AssetBulkUploadCheckDto(assets: [AssetBulkUploadCheckItem(checksum: "checksum_example", id: "id_example")]) // AssetBulkUploadCheckDto | 

// checkBulkUpload
AssetsAPI.checkBulkUpload(assetBulkUploadCheckDto: assetBulkUploadCheckDto) { (response, error) in
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
 **assetBulkUploadCheckDto** | [**AssetBulkUploadCheckDto**](AssetBulkUploadCheckDto.md) |  | 

### Return type

[**AssetBulkUploadCheckResponseDto**](AssetBulkUploadCheckResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **checkExistingAssets**
```swift
    open class func checkExistingAssets(checkExistingAssetsDto: CheckExistingAssetsDto, completion: @escaping (_ data: CheckExistingAssetsResponseDto?, _ error: Error?) -> Void)
```

checkExistingAssets

Checks if multiple assets exist on the server and returns all existing - used by background backup

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let checkExistingAssetsDto = CheckExistingAssetsDto(deviceAssetIds: ["deviceAssetIds_example"], deviceId: "deviceId_example") // CheckExistingAssetsDto | 

// checkExistingAssets
AssetsAPI.checkExistingAssets(checkExistingAssetsDto: checkExistingAssetsDto) { (response, error) in
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
 **checkExistingAssetsDto** | [**CheckExistingAssetsDto**](CheckExistingAssetsDto.md) |  | 

### Return type

[**CheckExistingAssetsResponseDto**](CheckExistingAssetsResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteAssets**
```swift
    open class func deleteAssets(assetBulkDeleteDto: AssetBulkDeleteDto, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let assetBulkDeleteDto = AssetBulkDeleteDto(force: false, ids: [123]) // AssetBulkDeleteDto | 

AssetsAPI.deleteAssets(assetBulkDeleteDto: assetBulkDeleteDto) { (response, error) in
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
 **assetBulkDeleteDto** | [**AssetBulkDeleteDto**](AssetBulkDeleteDto.md) |  | 

### Return type

Void (empty response body)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **downloadAsset**
```swift
    open class func downloadAsset(id: UUID, key: String? = nil, completion: @escaping (_ data: URL?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let key = "key_example" // String |  (optional)

AssetsAPI.downloadAsset(id: id, key: key) { (response, error) in
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

### Return type

**URL**

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getAllUserAssetsByDeviceId**
```swift
    open class func getAllUserAssetsByDeviceId(deviceId: String, completion: @escaping (_ data: [String]?, _ error: Error?) -> Void)
```

getAllUserAssetsByDeviceId

Get all asset of a device that are in the database, ID only.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let deviceId = "deviceId_example" // String | 

// getAllUserAssetsByDeviceId
AssetsAPI.getAllUserAssetsByDeviceId(deviceId: deviceId) { (response, error) in
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
 **deviceId** | **String** |  | 

### Return type

**[String]**

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getAssetInfo**
```swift
    open class func getAssetInfo(id: UUID, key: String? = nil, completion: @escaping (_ data: AssetResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let key = "key_example" // String |  (optional)

AssetsAPI.getAssetInfo(id: id, key: key) { (response, error) in
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

### Return type

[**AssetResponseDto**](AssetResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getAssetStatistics**
```swift
    open class func getAssetStatistics(isFavorite: Bool? = nil, isTrashed: Bool? = nil, visibility: AssetVisibility? = nil, completion: @escaping (_ data: AssetStatsResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let isFavorite = true // Bool |  (optional)
let isTrashed = true // Bool |  (optional)
let visibility = AssetVisibility() // AssetVisibility |  (optional)

AssetsAPI.getAssetStatistics(isFavorite: isFavorite, isTrashed: isTrashed, visibility: visibility) { (response, error) in
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
 **isFavorite** | **Bool** |  | [optional] 
 **isTrashed** | **Bool** |  | [optional] 
 **visibility** | [**AssetVisibility**](.md) |  | [optional] 

### Return type

[**AssetStatsResponseDto**](AssetStatsResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getRandom**
```swift
    open class func getRandom(count: Double? = nil, completion: @escaping (_ data: [AssetResponseDto]?, _ error: Error?) -> Void)
```



This property was deprecated in v1.116.0

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let count = 987 // Double |  (optional)

AssetsAPI.getRandom(count: count) { (response, error) in
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
 **count** | **Double** |  | [optional] 

### Return type

[**[AssetResponseDto]**](AssetResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **playAssetVideo**
```swift
    open class func playAssetVideo(id: UUID, key: String? = nil, completion: @escaping (_ data: URL?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let key = "key_example" // String |  (optional)

AssetsAPI.playAssetVideo(id: id, key: key) { (response, error) in
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

### Return type

**URL**

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **replaceAsset**
```swift
    open class func replaceAsset(id: UUID, assetData: URL, deviceAssetId: String, deviceId: String, fileCreatedAt: Date, fileModifiedAt: Date, key: String? = nil, duration: String? = nil, completion: @escaping (_ data: AssetMediaResponseDto?, _ error: Error?) -> Void)
```

replaceAsset

Replace the asset with new file, without changing its id

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let assetData = URL(string: "https://example.com")! // URL | 
let deviceAssetId = "deviceAssetId_example" // String | 
let deviceId = "deviceId_example" // String | 
let fileCreatedAt = Date() // Date | 
let fileModifiedAt = Date() // Date | 
let key = "key_example" // String |  (optional)
let duration = "duration_example" // String |  (optional)

// replaceAsset
AssetsAPI.replaceAsset(id: id, assetData: assetData, deviceAssetId: deviceAssetId, deviceId: deviceId, fileCreatedAt: fileCreatedAt, fileModifiedAt: fileModifiedAt, key: key, duration: duration) { (response, error) in
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
 **assetData** | **URL** |  | 
 **deviceAssetId** | **String** |  | 
 **deviceId** | **String** |  | 
 **fileCreatedAt** | **Date** |  | 
 **fileModifiedAt** | **Date** |  | 
 **key** | **String** |  | [optional] 
 **duration** | **String** |  | [optional] 

### Return type

[**AssetMediaResponseDto**](AssetMediaResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **runAssetJobs**
```swift
    open class func runAssetJobs(assetJobsDto: AssetJobsDto, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let assetJobsDto = AssetJobsDto(assetIds: [123], name: AssetJobName()) // AssetJobsDto | 

AssetsAPI.runAssetJobs(assetJobsDto: assetJobsDto) { (response, error) in
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
 **assetJobsDto** | [**AssetJobsDto**](AssetJobsDto.md) |  | 

### Return type

Void (empty response body)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateAsset**
```swift
    open class func updateAsset(id: UUID, updateAssetDto: UpdateAssetDto, completion: @escaping (_ data: AssetResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let updateAssetDto = UpdateAssetDto(dateTimeOriginal: "dateTimeOriginal_example", description: "description_example", isFavorite: false, latitude: 123, livePhotoVideoId: 123, longitude: 123, rating: 123, visibility: AssetVisibility()) // UpdateAssetDto | 

AssetsAPI.updateAsset(id: id, updateAssetDto: updateAssetDto) { (response, error) in
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
 **updateAssetDto** | [**UpdateAssetDto**](UpdateAssetDto.md) |  | 

### Return type

[**AssetResponseDto**](AssetResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateAssets**
```swift
    open class func updateAssets(assetBulkUpdateDto: AssetBulkUpdateDto, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let assetBulkUpdateDto = AssetBulkUpdateDto(dateTimeOriginal: "dateTimeOriginal_example", duplicateId: "duplicateId_example", ids: [123], isFavorite: false, latitude: 123, longitude: 123, rating: 123, visibility: AssetVisibility()) // AssetBulkUpdateDto | 

AssetsAPI.updateAssets(assetBulkUpdateDto: assetBulkUpdateDto) { (response, error) in
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
 **assetBulkUpdateDto** | [**AssetBulkUpdateDto**](AssetBulkUpdateDto.md) |  | 

### Return type

Void (empty response body)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **uploadAsset**
```swift
    open class func uploadAsset(assetData: URL, deviceAssetId: String, deviceId: String, fileCreatedAt: Date, fileModifiedAt: Date, key: String? = nil, xImmichChecksum: String? = nil, duration: String? = nil, isFavorite: Bool? = nil, livePhotoVideoId: UUID? = nil, sidecarData: URL? = nil, visibility: AssetVisibility? = nil, completion: @escaping (_ data: AssetMediaResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let assetData = URL(string: "https://example.com")! // URL | 
let deviceAssetId = "deviceAssetId_example" // String | 
let deviceId = "deviceId_example" // String | 
let fileCreatedAt = Date() // Date | 
let fileModifiedAt = Date() // Date | 
let key = "key_example" // String |  (optional)
let xImmichChecksum = "xImmichChecksum_example" // String | sha1 checksum that can be used for duplicate detection before the file is uploaded (optional)
let duration = "duration_example" // String |  (optional)
let isFavorite = true // Bool |  (optional)
let livePhotoVideoId = 987 // UUID |  (optional)
let sidecarData = URL(string: "https://example.com")! // URL |  (optional)
let visibility = AssetVisibility() // AssetVisibility |  (optional)

AssetsAPI.uploadAsset(assetData: assetData, deviceAssetId: deviceAssetId, deviceId: deviceId, fileCreatedAt: fileCreatedAt, fileModifiedAt: fileModifiedAt, key: key, xImmichChecksum: xImmichChecksum, duration: duration, isFavorite: isFavorite, livePhotoVideoId: livePhotoVideoId, sidecarData: sidecarData, visibility: visibility) { (response, error) in
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
 **assetData** | **URL** |  | 
 **deviceAssetId** | **String** |  | 
 **deviceId** | **String** |  | 
 **fileCreatedAt** | **Date** |  | 
 **fileModifiedAt** | **Date** |  | 
 **key** | **String** |  | [optional] 
 **xImmichChecksum** | **String** | sha1 checksum that can be used for duplicate detection before the file is uploaded | [optional] 
 **duration** | **String** |  | [optional] 
 **isFavorite** | **Bool** |  | [optional] 
 **livePhotoVideoId** | **UUID** |  | [optional] 
 **sidecarData** | **URL** |  | [optional] 
 **visibility** | [**AssetVisibility**](AssetVisibility.md) |  | [optional] 

### Return type

[**AssetMediaResponseDto**](AssetMediaResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **viewAsset**
```swift
    open class func viewAsset(id: UUID, key: String? = nil, size: AssetMediaSize? = nil, completion: @escaping (_ data: URL?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let key = "key_example" // String |  (optional)
let size = AssetMediaSize() // AssetMediaSize |  (optional)

AssetsAPI.viewAsset(id: id, key: key, size: size) { (response, error) in
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
 **size** | [**AssetMediaSize**](.md) |  | [optional] 

### Return type

**URL**

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

