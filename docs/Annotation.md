# Annotation

a holder/reference to the annotation on neurostore

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**neurostore_id** | **string** | the id of the annotation on neurostore | [optional] [default to undefined]
**snapshot** | **object** | the snapshot taken of the annotation pending a successful run of the meta-analytic algorithm | [optional] [default to undefined]
**studyset** | **string** | The related cached studyset to this annotation. | [optional] [readonly] [default to undefined]
**neurostore_url** | **string** |  | [optional] [readonly] [default to undefined]

## Example

```typescript
import { Annotation } from './api';

const instance: Annotation = {
    neurostore_id,
    snapshot,
    studyset,
    neurostore_url,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
