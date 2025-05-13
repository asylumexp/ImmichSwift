# AssetResponseDto

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**checksum** | **String** | base64 encoded sha1 hash | 
**deviceAssetId** | **String** |  | 
**deviceId** | **String** |  | 
**duplicateId** | **String** |  | [optional] 
**duration** | **String** |  | 
**exifInfo** | [**ExifResponseDto**](ExifResponseDto.md) |  | [optional] 
**fileCreatedAt** | **Date** |  | 
**fileModifiedAt** | **Date** |  | 
**hasMetadata** | **Bool** |  | 
**id** | **String** |  | 
**isArchived** | **Bool** |  | 
**isFavorite** | **Bool** |  | 
**isOffline** | **Bool** |  | 
**isTrashed** | **Bool** |  | 
**libraryId** | **String** | This property was deprecated in v1.106.0 | [optional] 
**livePhotoVideoId** | **String** |  | [optional] 
**localDateTime** | **Date** |  | 
**originalFileName** | **String** |  | 
**originalMimeType** | **String** |  | [optional] 
**originalPath** | **String** |  | 
**owner** | [**UserResponseDto**](UserResponseDto.md) |  | [optional] 
**ownerId** | **String** |  | 
**people** | [PersonWithFacesResponseDto] |  | [optional] 
**resized** | **Bool** | This property was deprecated in v1.113.0 | [optional] 
**stack** | [**AssetStackResponseDto**](AssetStackResponseDto.md) |  | [optional] 
**tags** | [TagResponseDto] |  | [optional] 
**thumbhash** | **String** |  | 
**type** | [**AssetTypeEnum**](AssetTypeEnum.md) |  | 
**unassignedFaces** | [AssetFaceWithoutPersonResponseDto] |  | [optional] 
**updatedAt** | **Date** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


