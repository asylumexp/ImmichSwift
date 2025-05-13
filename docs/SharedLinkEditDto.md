# SharedLinkEditDto

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**allowDownload** | **Bool** |  | [optional] 
**allowUpload** | **Bool** |  | [optional] 
**changeExpiryTime** | **Bool** | Few clients cannot send null to set the expiryTime to never. Setting this flag and not sending expiryAt is considered as null instead. Clients that can send null values can ignore this. | [optional] 
**description** | **String** |  | [optional] 
**expiresAt** | **Date** |  | [optional] 
**password** | **String** |  | [optional] 
**showMetadata** | **Bool** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


