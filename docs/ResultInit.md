# ResultInit


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**meta_analysis_id** | **string** |  | [optional] [default to undefined]
**snapshot_studyset** | **object** |  | [optional] [default to undefined]
**snapshot_annotation** | **object** |  | [optional] [default to undefined]
**snapshot_studyset_id** | **string** | ID of an existing cached studyset snapshot to link to this result. | [optional] [default to undefined]
**snapshot_annotation_id** | **string** | ID of an existing cached annotation snapshot to link to this result. | [optional] [default to undefined]
**cli_version** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { ResultInit } from './api';

const instance: ResultInit = {
    meta_analysis_id,
    snapshot_studyset,
    snapshot_annotation,
    snapshot_studyset_id,
    snapshot_annotation_id,
    cli_version,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
