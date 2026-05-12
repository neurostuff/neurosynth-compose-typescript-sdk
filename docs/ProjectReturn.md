# ProjectReturn


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | the identifier for the resource. | [optional] [default to undefined]
**updated_at** | **string** | when the resource was last modified. | [optional] [readonly] [default to undefined]
**created_at** | **string** | When the resource was created. | [optional] [readonly] [default to undefined]
**user** | **string** | Who owns the resource. | [optional] [default to undefined]
**username** | **string** |  | [optional] [readonly] [default to undefined]
**provenance** | **object** |  | [optional] [default to undefined]
**meta_analyses** | [**ProjectMetaAnalyses**](ProjectMetaAnalyses.md) |  | [optional] [default to undefined]
**name** | **string** |  | [optional] [default to undefined]
**description** | **string** |  | [optional] [default to undefined]
**_public** | **boolean** | whether the project is public or private | [optional] [default to undefined]
**neurostore_study** | [**NeurostoreStudy**](NeurostoreStudy.md) |  | [optional] [default to undefined]
**neurostore_url** | **string** |  | [optional] [default to undefined]
**draft** | **boolean** |  | [optional] [readonly] [default to undefined]

## Example

```typescript
import { ProjectReturn } from './api';

const instance: ProjectReturn = {
    id,
    updated_at,
    created_at,
    user,
    username,
    provenance,
    meta_analyses,
    name,
    description,
    _public,
    neurostore_study,
    neurostore_url,
    draft,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
