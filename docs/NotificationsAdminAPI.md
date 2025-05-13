# NotificationsAdminAPI

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createNotification**](NotificationsAdminAPI.md#createnotification) | **POST** /admin/notifications | 
[**getNotificationTemplateAdmin**](NotificationsAdminAPI.md#getnotificationtemplateadmin) | **POST** /admin/notifications/templates/{name} | 
[**sendTestEmailAdmin**](NotificationsAdminAPI.md#sendtestemailadmin) | **POST** /admin/notifications/test-email | 


# **createNotification**
```swift
    open class func createNotification(notificationCreateDto: NotificationCreateDto, completion: @escaping (_ data: NotificationDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let notificationCreateDto = NotificationCreateDto(data: 123, description: "description_example", level: NotificationLevel(), readAt: Date(), title: "title_example", type: NotificationType(), userId: 123) // NotificationCreateDto | 

NotificationsAdminAPI.createNotification(notificationCreateDto: notificationCreateDto) { (response, error) in
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
 **notificationCreateDto** | [**NotificationCreateDto**](NotificationCreateDto.md) |  | 

### Return type

[**NotificationDto**](NotificationDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getNotificationTemplateAdmin**
```swift
    open class func getNotificationTemplateAdmin(name: String, templateDto: TemplateDto, completion: @escaping (_ data: TemplateResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let name = "name_example" // String | 
let templateDto = TemplateDto(template: "template_example") // TemplateDto | 

NotificationsAdminAPI.getNotificationTemplateAdmin(name: name, templateDto: templateDto) { (response, error) in
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
 **templateDto** | [**TemplateDto**](TemplateDto.md) |  | 

### Return type

[**TemplateResponseDto**](TemplateResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **sendTestEmailAdmin**
```swift
    open class func sendTestEmailAdmin(systemConfigSmtpDto: SystemConfigSmtpDto, completion: @escaping (_ data: TestEmailResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let systemConfigSmtpDto = SystemConfigSmtpDto(enabled: false, from: "from_example", replyTo: "replyTo_example", transport: SystemConfigSmtpTransportDto(host: "host_example", ignoreCert: false, password: "password_example", port: 123, username: "username_example")) // SystemConfigSmtpDto | 

NotificationsAdminAPI.sendTestEmailAdmin(systemConfigSmtpDto: systemConfigSmtpDto) { (response, error) in
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
 **systemConfigSmtpDto** | [**SystemConfigSmtpDto**](SystemConfigSmtpDto.md) |  | 

### Return type

[**TestEmailResponseDto**](TestEmailResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

