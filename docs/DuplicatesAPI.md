# DuplicatesAPI

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getAssetDuplicates**](DuplicatesAPI.md#getassetduplicates) | **GET** /duplicates | 


# **getAssetDuplicates**
```swift
    open class func getAssetDuplicates(completion: @escaping (_ data: [DuplicateResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient


DuplicatesAPI.getAssetDuplicates() { (response, error) in
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

[**[DuplicateResponseDto]**](DuplicateResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

