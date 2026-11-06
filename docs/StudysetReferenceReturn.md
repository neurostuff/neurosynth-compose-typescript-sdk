# StudysetReferenceReturn


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**studysets** | [**Array&lt;StudysetSnapshotSummary&gt;**](StudysetSnapshotSummary.md) |  | [optional] [default to undefined]
**id** | **string** | the identifier for the resource. | [optional] [default to undefined]
**updated_at** | **string** | when the resource was last modified. | [optional] [readonly] [default to undefined]
**created_at** | **string** | When the resource was created. | [optional] [readonly] [default to undefined]
**user** | **string** | The owner\&#39;s Auth0 id, served only to the owner; null for anyone else, who sees &#x60;username&#x60;. | [optional] [default to undefined]
**username** | **string** |  | [optional] [readonly] [default to undefined]

## Example

```typescript
import { StudysetReferenceReturn } from './api';

const instance: StudysetReferenceReturn = {
    studysets,
    id,
    updated_at,
    created_at,
    user,
    username,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
