# OAuthAPI

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**finishOAuth**](OAuthAPI.md#finishoauth) | **POST** /oauth/callback | 
[**linkOAuthAccount**](OAuthAPI.md#linkoauthaccount) | **POST** /oauth/link | 
[**redirectOAuthToMobile**](OAuthAPI.md#redirectoauthtomobile) | **GET** /oauth/mobile-redirect | 
[**startOAuth**](OAuthAPI.md#startoauth) | **POST** /oauth/authorize | 
[**unlinkOAuthAccount**](OAuthAPI.md#unlinkoauthaccount) | **POST** /oauth/unlink | 


# **finishOAuth**
```swift
    open class func finishOAuth(oAuthCallbackDto: OAuthCallbackDto, completion: @escaping (_ data: LoginResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let oAuthCallbackDto = OAuthCallbackDto(codeVerifier: "codeVerifier_example", state: "state_example", url: "url_example") // OAuthCallbackDto | 

OAuthAPI.finishOAuth(oAuthCallbackDto: oAuthCallbackDto) { (response, error) in
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
 **oAuthCallbackDto** | [**OAuthCallbackDto**](OAuthCallbackDto.md) |  | 

### Return type

[**LoginResponseDto**](LoginResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **linkOAuthAccount**
```swift
    open class func linkOAuthAccount(oAuthCallbackDto: OAuthCallbackDto, completion: @escaping (_ data: UserAdminResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let oAuthCallbackDto = OAuthCallbackDto(codeVerifier: "codeVerifier_example", state: "state_example", url: "url_example") // OAuthCallbackDto | 

OAuthAPI.linkOAuthAccount(oAuthCallbackDto: oAuthCallbackDto) { (response, error) in
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
 **oAuthCallbackDto** | [**OAuthCallbackDto**](OAuthCallbackDto.md) |  | 

### Return type

[**UserAdminResponseDto**](UserAdminResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **redirectOAuthToMobile**
```swift
    open class func redirectOAuthToMobile(completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient


OAuthAPI.redirectOAuthToMobile() { (response, error) in
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

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **startOAuth**
```swift
    open class func startOAuth(oAuthConfigDto: OAuthConfigDto, completion: @escaping (_ data: OAuthAuthorizeResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let oAuthConfigDto = OAuthConfigDto(codeChallenge: "codeChallenge_example", redirectUri: "redirectUri_example", state: "state_example") // OAuthConfigDto | 

OAuthAPI.startOAuth(oAuthConfigDto: oAuthConfigDto) { (response, error) in
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
 **oAuthConfigDto** | [**OAuthConfigDto**](OAuthConfigDto.md) |  | 

### Return type

[**OAuthAuthorizeResponseDto**](OAuthAuthorizeResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **unlinkOAuthAccount**
```swift
    open class func unlinkOAuthAccount(completion: @escaping (_ data: UserAdminResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient


OAuthAPI.unlinkOAuthAccount() { (response, error) in
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

[**UserAdminResponseDto**](UserAdminResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

