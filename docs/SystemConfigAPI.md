# SystemConfigAPI

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getConfig**](SystemConfigAPI.md#getconfig) | **GET** /system-config | 
[**getConfigDefaults**](SystemConfigAPI.md#getconfigdefaults) | **GET** /system-config/defaults | 
[**getStorageTemplateOptions**](SystemConfigAPI.md#getstoragetemplateoptions) | **GET** /system-config/storage-template-options | 
[**updateConfig**](SystemConfigAPI.md#updateconfig) | **PUT** /system-config | 


# **getConfig**
```swift
    open class func getConfig(completion: @escaping (_ data: SystemConfigDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient


SystemConfigAPI.getConfig() { (response, error) in
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

[**SystemConfigDto**](SystemConfigDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getConfigDefaults**
```swift
    open class func getConfigDefaults(completion: @escaping (_ data: SystemConfigDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient


SystemConfigAPI.getConfigDefaults() { (response, error) in
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

[**SystemConfigDto**](SystemConfigDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getStorageTemplateOptions**
```swift
    open class func getStorageTemplateOptions(completion: @escaping (_ data: SystemConfigTemplateStorageOptionDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient


SystemConfigAPI.getStorageTemplateOptions() { (response, error) in
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

[**SystemConfigTemplateStorageOptionDto**](SystemConfigTemplateStorageOptionDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateConfig**
```swift
    open class func updateConfig(systemConfigDto: SystemConfigDto, completion: @escaping (_ data: SystemConfigDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let systemConfigDto = SystemConfigDto(backup: SystemConfigBackupsDto(database: DatabaseBackupConfig(cronExpression: "cronExpression_example", enabled: false, keepLastAmount: 123)), ffmpeg: SystemConfigFFmpegDto(accel: TranscodeHWAccel(), accelDecode: false, acceptedAudioCodecs: [AudioCodec()], acceptedContainers: [VideoContainer()], acceptedVideoCodecs: [VideoCodec()], bframes: 123, cqMode: CQMode(), crf: 123, gopSize: 123, maxBitrate: "maxBitrate_example", preferredHwDevice: "preferredHwDevice_example", preset: "preset_example", refs: 123, targetAudioCodec: nil, targetResolution: "targetResolution_example", targetVideoCodec: nil, temporalAQ: false, threads: 123, tonemap: ToneMapping(), transcode: TranscodePolicy(), twoPass: false), image: SystemConfigImageDto(colorspace: Colorspace(), extractEmbedded: false, fullsize: SystemConfigGeneratedFullsizeImageDto(enabled: false, format: ImageFormat(), quality: 123), preview: SystemConfigGeneratedImageDto(format: nil, quality: 123, size: 123), thumbnail: nil), job: SystemConfigJobDto(backgroundTask: JobSettingsDto(concurrency: 123), faceDetection: nil, library: nil, metadataExtraction: nil, migration: nil, notifications: nil, search: nil, sidecar: nil, smartSearch: nil, thumbnailGeneration: nil, videoConversion: nil), library: SystemConfigLibraryDto(scan: SystemConfigLibraryScanDto(cronExpression: "cronExpression_example", enabled: false), watch: SystemConfigLibraryWatchDto(enabled: false)), logging: SystemConfigLoggingDto(enabled: false, level: LogLevel()), machineLearning: SystemConfigMachineLearningDto(clip: CLIPConfig(enabled: false, modelName: "modelName_example"), duplicateDetection: DuplicateDetectionConfig(enabled: false, maxDistance: 123), enabled: false, facialRecognition: FacialRecognitionConfig(enabled: false, maxDistance: 123, minFaces: 123, minScore: 123, modelName: "modelName_example"), url: "url_example", urls: ["urls_example"]), map: SystemConfigMapDto(darkStyle: "darkStyle_example", enabled: false, lightStyle: "lightStyle_example"), metadata: SystemConfigMetadataDto(faces: SystemConfigFacesDto(_import: false)), newVersionCheck: SystemConfigNewVersionCheckDto(enabled: false), notifications: SystemConfigNotificationsDto(smtp: SystemConfigSmtpDto(enabled: false, from: "from_example", replyTo: "replyTo_example", transport: SystemConfigSmtpTransportDto(host: "host_example", ignoreCert: false, password: "password_example", port: 123, username: "username_example"))), oauth: SystemConfigOAuthDto(autoLaunch: false, autoRegister: false, buttonText: "buttonText_example", clientId: "clientId_example", clientSecret: "clientSecret_example", defaultStorageQuota: 123, enabled: false, issuerUrl: "issuerUrl_example", mobileOverrideEnabled: false, mobileRedirectUri: "mobileRedirectUri_example", profileSigningAlgorithm: "profileSigningAlgorithm_example", scope: "scope_example", signingAlgorithm: "signingAlgorithm_example", storageLabelClaim: "storageLabelClaim_example", storageQuotaClaim: "storageQuotaClaim_example", timeout: 123, tokenEndpointAuthMethod: OAuthTokenEndpointAuthMethod()), passwordLogin: SystemConfigPasswordLoginDto(enabled: false), reverseGeocoding: SystemConfigReverseGeocodingDto(enabled: false), server: SystemConfigServerDto(externalDomain: "externalDomain_example", loginPageMessage: "loginPageMessage_example", publicUsers: false), storageTemplate: SystemConfigStorageTemplateDto(enabled: false, hashVerificationEnabled: false, template: "template_example"), templates: SystemConfigTemplatesDto(email: SystemConfigTemplateEmailsDto(albumInviteTemplate: "albumInviteTemplate_example", albumUpdateTemplate: "albumUpdateTemplate_example", welcomeTemplate: "welcomeTemplate_example")), theme: SystemConfigThemeDto(customCss: "customCss_example"), trash: SystemConfigTrashDto(days: 123, enabled: false), user: SystemConfigUserDto(deleteDelay: 123)) // SystemConfigDto | 

SystemConfigAPI.updateConfig(systemConfigDto: systemConfigDto) { (response, error) in
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
 **systemConfigDto** | [**SystemConfigDto**](SystemConfigDto.md) |  | 

### Return type

[**SystemConfigDto**](SystemConfigDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

