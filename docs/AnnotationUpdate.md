# AnnotationUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**neurostore_id** | **string** | the id of the annotation on neurostore | [optional] [default to undefined]
**snapshot** | **object** | the snapshot taken of the annotation pending a successful run of the meta-analytic algorithm | [optional] [default to undefined]
**snapshot_studyset** | [**StudysetSnapshotSummary**](StudysetSnapshotSummary.md) |  | [optional] [default to undefined]
**neurostore_url** | **string** |  | [optional] [readonly] [default to undefined]
**snapshot_studyset_id** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { AnnotationUpdate } from './api';

const instance: AnnotationUpdate = {
    neurostore_id,
    snapshot,
    snapshot_studyset,
    neurostore_url,
    snapshot_studyset_id,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
