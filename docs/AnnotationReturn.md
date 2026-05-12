# AnnotationReturn


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**neurostore_id** | **string** | the id of the annotation on neurostore | [optional] [default to undefined]
**snapshot** | **object** | the snapshot taken of the annotation pending a successful run of the meta-analytic algorithm | [optional] [default to undefined]
**studyset** | **string** | The related cached studyset to this annotation. | [optional] [readonly] [default to undefined]
**neurostore_url** | **string** |  | [optional] [readonly] [default to undefined]
**id** | **string** | the identifier for the resource. | [optional] [default to undefined]
**updated_at** | **string** | when the resource was last modified. | [optional] [readonly] [default to undefined]
**created_at** | **string** | When the resource was created. | [optional] [readonly] [default to undefined]
**user** | **string** | Who owns the resource. | [optional] [default to undefined]
**username** | **string** |  | [optional] [readonly] [default to undefined]

## Example

```typescript
import { AnnotationReturn } from './api';

const instance: AnnotationReturn = {
    neurostore_id,
    snapshot,
    studyset,
    neurostore_url,
    id,
    updated_at,
    created_at,
    user,
    username,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
