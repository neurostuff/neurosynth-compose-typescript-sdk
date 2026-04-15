# ResultInit


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**meta_analysis_id** | **string** |  | [optional] [default to undefined]
**cached_studyset** | **object** |  | [optional] [default to undefined]
**cached_annotation** | **object** |  | [optional] [default to undefined]
**cached_studyset_id** | **string** | ID of an existing cached studyset snapshot to link to this result. | [optional] [default to undefined]
**cached_annotation_id** | **string** | ID of an existing cached annotation snapshot to link to this result. | [optional] [default to undefined]
**cli_version** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { ResultInit } from './api';

const instance: ResultInit = {
    meta_analysis_id,
    cached_studyset,
    cached_annotation,
    cached_studyset_id,
    cached_annotation_id,
    cli_version,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
