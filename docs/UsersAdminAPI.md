# UsersAdminAPI

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createUserAdmin**](UsersAdminAPI.md#createuseradmin) | **POST** /admin/users | 
[**deleteUserAdmin**](UsersAdminAPI.md#deleteuseradmin) | **DELETE** /admin/users/{id} | 
[**getUserAdmin**](UsersAdminAPI.md#getuseradmin) | **GET** /admin/users/{id} | 
[**getUserPreferencesAdmin**](UsersAdminAPI.md#getuserpreferencesadmin) | **GET** /admin/users/{id}/preferences | 
[**getUserStatisticsAdmin**](UsersAdminAPI.md#getuserstatisticsadmin) | **GET** /admin/users/{id}/statistics | 
[**restoreUserAdmin**](UsersAdminAPI.md#restoreuseradmin) | **POST** /admin/users/{id}/restore | 
[**searchUsersAdmin**](UsersAdminAPI.md#searchusersadmin) | **GET** /admin/users | 
[**updateUserAdmin**](UsersAdminAPI.md#updateuseradmin) | **PUT** /admin/users/{id} | 
[**updateUserPreferencesAdmin**](UsersAdminAPI.md#updateuserpreferencesadmin) | **PUT** /admin/users/{id}/preferences | 


# **createUserAdmin**
```swift
    open class func createUserAdmin(userAdminCreateDto: UserAdminCreateDto, completion: @escaping (_ data: UserAdminResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let userAdminCreateDto = UserAdminCreateDto(avatarColor: UserAvatarColor(), email: "email_example", name: "name_example", notify: false, password: "password_example", quotaSizeInBytes: 123, shouldChangePassword: false, storageLabel: "storageLabel_example") // UserAdminCreateDto | 

UsersAdminAPI.createUserAdmin(userAdminCreateDto: userAdminCreateDto) { (response, error) in
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
 **userAdminCreateDto** | [**UserAdminCreateDto**](UserAdminCreateDto.md) |  | 

### Return type

[**UserAdminResponseDto**](UserAdminResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteUserAdmin**
```swift
    open class func deleteUserAdmin(id: UUID, userAdminDeleteDto: UserAdminDeleteDto, completion: @escaping (_ data: UserAdminResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let userAdminDeleteDto = UserAdminDeleteDto(force: false) // UserAdminDeleteDto | 

UsersAdminAPI.deleteUserAdmin(id: id, userAdminDeleteDto: userAdminDeleteDto) { (response, error) in
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
 **userAdminDeleteDto** | [**UserAdminDeleteDto**](UserAdminDeleteDto.md) |  | 

### Return type

[**UserAdminResponseDto**](UserAdminResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getUserAdmin**
```swift
    open class func getUserAdmin(id: UUID, completion: @escaping (_ data: UserAdminResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 

UsersAdminAPI.getUserAdmin(id: id) { (response, error) in
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

[**UserAdminResponseDto**](UserAdminResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getUserPreferencesAdmin**
```swift
    open class func getUserPreferencesAdmin(id: UUID, completion: @escaping (_ data: UserPreferencesResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 

UsersAdminAPI.getUserPreferencesAdmin(id: id) { (response, error) in
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

[**UserPreferencesResponseDto**](UserPreferencesResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getUserStatisticsAdmin**
```swift
    open class func getUserStatisticsAdmin(id: UUID, isFavorite: Bool? = nil, isTrashed: Bool? = nil, visibility: AssetVisibility? = nil, completion: @escaping (_ data: AssetStatsResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let isFavorite = true // Bool |  (optional)
let isTrashed = true // Bool |  (optional)
let visibility = AssetVisibility() // AssetVisibility |  (optional)

UsersAdminAPI.getUserStatisticsAdmin(id: id, isFavorite: isFavorite, isTrashed: isTrashed, visibility: visibility) { (response, error) in
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

# **restoreUserAdmin**
```swift
    open class func restoreUserAdmin(id: UUID, completion: @escaping (_ data: UserAdminResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 

UsersAdminAPI.restoreUserAdmin(id: id) { (response, error) in
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

[**UserAdminResponseDto**](UserAdminResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **searchUsersAdmin**
```swift
    open class func searchUsersAdmin(id: UUID? = nil, withDeleted: Bool? = nil, completion: @escaping (_ data: [UserAdminResponseDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID |  (optional)
let withDeleted = true // Bool |  (optional)

UsersAdminAPI.searchUsersAdmin(id: id, withDeleted: withDeleted) { (response, error) in
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
 **id** | **UUID** |  | [optional] 
 **withDeleted** | **Bool** |  | [optional] 

### Return type

[**[UserAdminResponseDto]**](UserAdminResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateUserAdmin**
```swift
    open class func updateUserAdmin(id: UUID, userAdminUpdateDto: UserAdminUpdateDto, completion: @escaping (_ data: UserAdminResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let userAdminUpdateDto = UserAdminUpdateDto(avatarColor: UserAvatarColor(), email: "email_example", name: "name_example", password: "password_example", pinCode: "pinCode_example", quotaSizeInBytes: 123, shouldChangePassword: false, storageLabel: "storageLabel_example") // UserAdminUpdateDto | 

UsersAdminAPI.updateUserAdmin(id: id, userAdminUpdateDto: userAdminUpdateDto) { (response, error) in
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
 **userAdminUpdateDto** | [**UserAdminUpdateDto**](UserAdminUpdateDto.md) |  | 

### Return type

[**UserAdminResponseDto**](UserAdminResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateUserPreferencesAdmin**
```swift
    open class func updateUserPreferencesAdmin(id: UUID, userPreferencesUpdateDto: UserPreferencesUpdateDto, completion: @escaping (_ data: UserPreferencesResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let userPreferencesUpdateDto = UserPreferencesUpdateDto(avatar: AvatarUpdate(color: UserAvatarColor()), download: DownloadUpdate(archiveSize: 123, includeEmbeddedVideos: false), emailNotifications: EmailNotificationsUpdate(albumInvite: false, albumUpdate: false, enabled: false), folders: FoldersUpdate(enabled: false, sidebarWeb: false), memories: MemoriesUpdate(enabled: false), people: PeopleUpdate(enabled: false, sidebarWeb: false), purchase: PurchaseUpdate(hideBuyButtonUntil: "hideBuyButtonUntil_example", showSupportBadge: false), ratings: RatingsUpdate(enabled: false), sharedLinks: SharedLinksUpdate(enabled: false, sidebarWeb: false), tags: TagsUpdate(enabled: false, sidebarWeb: false)) // UserPreferencesUpdateDto | 

UsersAdminAPI.updateUserPreferencesAdmin(id: id, userPreferencesUpdateDto: userPreferencesUpdateDto) { (response, error) in
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
 **userPreferencesUpdateDto** | [**UserPreferencesUpdateDto**](UserPreferencesUpdateDto.md) |  | 

### Return type

[**UserPreferencesResponseDto**](UserPreferencesResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

