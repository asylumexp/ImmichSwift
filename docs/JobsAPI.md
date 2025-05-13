# JobsAPI

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createJob**](JobsAPI.md#createjob) | **POST** /jobs | 
[**getAllJobsStatus**](JobsAPI.md#getalljobsstatus) | **GET** /jobs | 
[**sendJobCommand**](JobsAPI.md#sendjobcommand) | **PUT** /jobs/{id} | 


# **createJob**
```swift
    open class func createJob(jobCreateDto: JobCreateDto, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let jobCreateDto = JobCreateDto(name: ManualJobName()) // JobCreateDto | 

JobsAPI.createJob(jobCreateDto: jobCreateDto) { (response, error) in
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
 **jobCreateDto** | [**JobCreateDto**](JobCreateDto.md) |  | 

### Return type

Void (empty response body)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getAllJobsStatus**
```swift
    open class func getAllJobsStatus(completion: @escaping (_ data: AllJobStatusResponseDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient


JobsAPI.getAllJobsStatus() { (response, error) in
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

[**AllJobStatusResponseDto**](AllJobStatusResponseDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **sendJobCommand**
```swift
    open class func sendJobCommand(id: JobName, jobCommandDto: JobCommandDto, completion: @escaping (_ data: JobStatusDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let id = JobName() // JobName | 
let jobCommandDto = JobCommandDto(command: JobCommand(), force: false) // JobCommandDto | 

JobsAPI.sendJobCommand(id: id, jobCommandDto: jobCommandDto) { (response, error) in
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
 **id** | [**JobName**](.md) |  | 
 **jobCommandDto** | [**JobCommandDto**](JobCommandDto.md) |  | 

### Return type

[**JobStatusDto**](JobStatusDto.md)

### Authorization

[cookie](../README.md#cookie), [api_key](../README.md#api_key), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

