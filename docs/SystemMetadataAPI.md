# SystemMetadataAPI

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getAdminOnboarding**](SystemMetadataAPI.md#getadminonboarding) | **GET** /system-metadata/admin-onboarding | 
[**getReverseGeocodingState**](SystemMetadataAPI.md#getreversegeocodingstate) | **GET** /system-metadata/reverse-geocoding-state | 
[**updateAdminOnboarding**](SystemMetadataAPI.md#updateadminonboarding) | **POST** /system-metadata/admin-onboarding | 


# **getAdminOnboarding**
```swift
    open class func getAdminOnboarding(completion: @escaping (_ data: AdminOnboardingUpdateDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient


SystemMetadataAPI.getAdminOnboarding() { (response, error) in
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

[**AdminOnboardingUpdateDto**](AdminOnboardingUpdateDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getReverseGeocodingState**
```swift
    open class func getReverseGeocodingState(completion: @escaping (_ data: ReverseGeocodingStateResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient


SystemMetadataAPI.getReverseGeocodingState() { (response, error) in
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

[**ReverseGeocodingStateResponseDto**](ReverseGeocodingStateResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateAdminOnboarding**
```swift
    open class func updateAdminOnboarding(adminOnboardingUpdateDto: AdminOnboardingUpdateDto, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let adminOnboardingUpdateDto = AdminOnboardingUpdateDto(isOnboarded: false) // AdminOnboardingUpdateDto | 

SystemMetadataAPI.updateAdminOnboarding(adminOnboardingUpdateDto: adminOnboardingUpdateDto) { (response, error) in
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
 **adminOnboardingUpdateDto** | [**AdminOnboardingUpdateDto**](AdminOnboardingUpdateDto.md) |  | 

### Return type

Void (empty response body)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

