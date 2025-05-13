# DeprecatedAPI

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getRandom**](DeprecatedAPI.md#getrandom) | **GET** /assets/random | 


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

DeprecatedAPI.getRandom(count: count) { (response, error) in
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

