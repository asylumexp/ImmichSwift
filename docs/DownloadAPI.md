# DownloadAPI

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**downloadArchive**](DownloadAPI.md#downloadarchive) | **POST** /download/archive | 
[**getDownloadInfo**](DownloadAPI.md#getdownloadinfo) | **POST** /download/info | 


# **downloadArchive**
```swift
    open class func downloadArchive(assetIdsDto: AssetIdsDto, key: String? = nil, completion: @escaping (_ data: URL?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let assetIdsDto = AssetIdsDto(assetIds: [123]) // AssetIdsDto | 
let key = "key_example" // String |  (optional)

DownloadAPI.downloadArchive(assetIdsDto: assetIdsDto, key: key) { (response, error) in
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
 **assetIdsDto** | [**AssetIdsDto**](AssetIdsDto.md) |  | 
 **key** | **String** |  | [optional] 

### Return type

**URL**

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getDownloadInfo**
```swift
    open class func getDownloadInfo(downloadInfoDto: DownloadInfoDto, key: String? = nil, completion: @escaping (_ data: DownloadResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let downloadInfoDto = DownloadInfoDto(albumId: 123, archiveSize: 123, assetIds: [123], userId: 123) // DownloadInfoDto | 
let key = "key_example" // String |  (optional)

DownloadAPI.getDownloadInfo(downloadInfoDto: downloadInfoDto, key: key) { (response, error) in
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
 **downloadInfoDto** | [**DownloadInfoDto**](DownloadInfoDto.md) |  | 
 **key** | **String** |  | [optional] 

### Return type

[**DownloadResponseDto**](DownloadResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

