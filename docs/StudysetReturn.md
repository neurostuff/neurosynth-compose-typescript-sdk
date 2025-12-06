# StudysetReturn


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**neurostore_id** | **string** | The id of the studyset on neurostore. | [optional] [default to undefined]
**snapshot** | **object** | The snapshot of the studyset pending a successful run of the meta-analysis. | [optional] [default to undefined]
**neurostore_url** | **string** |  | [optional] [readonly] [default to undefined]
**version** | **string** | A string representing a labeled version of this particular studyset. | [optional] [default to undefined]
**id** | **string** | the identifier for the resource. | [optional] [default to undefined]
**updated_at** | **string** | when the resource was last modified. | [optional] [readonly] [default to undefined]
**created_at** | **string** | When the resource was created. | [optional] [readonly] [default to undefined]
**user** | **string** | Who owns the resource. | [optional] [default to undefined]
**username** | **string** |  | [optional] [readonly] [default to undefined]

## Example

```typescript
import { StudysetReturn } from './api';

const instance: StudysetReturn = {
    neurostore_id,
    snapshot,
    neurostore_url,
    version,
    id,
    updated_at,
    created_at,
    user,
    username,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
