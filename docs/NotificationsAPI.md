# NotificationsAPI

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteNotification**](NotificationsAPI.md#deletenotification) | **DELETE** /notifications/{id} | 
[**deleteNotifications**](NotificationsAPI.md#deletenotifications) | **DELETE** /notifications | 
[**getNotification**](NotificationsAPI.md#getnotification) | **GET** /notifications/{id} | 
[**getNotifications**](NotificationsAPI.md#getnotifications) | **GET** /notifications | 
[**updateNotification**](NotificationsAPI.md#updatenotification) | **PUT** /notifications/{id} | 
[**updateNotifications**](NotificationsAPI.md#updatenotifications) | **PUT** /notifications | 


# **deleteNotification**
```swift
    open class func deleteNotification(id: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 

NotificationsAPI.deleteNotification(id: id) { (response, error) in
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

Void (empty response body)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteNotifications**
```swift
    open class func deleteNotifications(notificationDeleteAllDto: NotificationDeleteAllDto, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let notificationDeleteAllDto = NotificationDeleteAllDto(ids: [123]) // NotificationDeleteAllDto | 

NotificationsAPI.deleteNotifications(notificationDeleteAllDto: notificationDeleteAllDto) { (response, error) in
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
 **notificationDeleteAllDto** | [**NotificationDeleteAllDto**](NotificationDeleteAllDto.md) |  | 

### Return type

Void (empty response body)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getNotification**
```swift
    open class func getNotification(id: UUID, completion: @escaping (_ data: NotificationDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 

NotificationsAPI.getNotification(id: id) { (response, error) in
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

[**NotificationDto**](NotificationDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getNotifications**
```swift
    open class func getNotifications(id: UUID? = nil, level: NotificationLevel? = nil, type: NotificationType? = nil, unread: Bool? = nil, completion: @escaping (_ data: [NotificationDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID |  (optional)
let level = NotificationLevel() // NotificationLevel |  (optional)
let type = NotificationType() // NotificationType |  (optional)
let unread = true // Bool |  (optional)

NotificationsAPI.getNotifications(id: id, level: level, type: type, unread: unread) { (response, error) in
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
 **level** | [**NotificationLevel**](.md) |  | [optional] 
 **type** | [**NotificationType**](.md) |  | [optional] 
 **unread** | **Bool** |  | [optional] 

### Return type

[**[NotificationDto]**](NotificationDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateNotification**
```swift
    open class func updateNotification(id: UUID, notificationUpdateDto: NotificationUpdateDto, completion: @escaping (_ data: NotificationDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = 987 // UUID | 
let notificationUpdateDto = NotificationUpdateDto(readAt: Date()) // NotificationUpdateDto | 

NotificationsAPI.updateNotification(id: id, notificationUpdateDto: notificationUpdateDto) { (response, error) in
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
 **notificationUpdateDto** | [**NotificationUpdateDto**](NotificationUpdateDto.md) |  | 

### Return type

[**NotificationDto**](NotificationDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateNotifications**
```swift
    open class func updateNotifications(notificationUpdateAllDto: NotificationUpdateAllDto, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let notificationUpdateAllDto = NotificationUpdateAllDto(ids: [123], readAt: Date()) // NotificationUpdateAllDto | 

NotificationsAPI.updateNotifications(notificationUpdateAllDto: notificationUpdateAllDto) { (response, error) in
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
 **notificationUpdateAllDto** | [**NotificationUpdateAllDto**](NotificationUpdateAllDto.md) |  | 

### Return type

Void (empty response body)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

