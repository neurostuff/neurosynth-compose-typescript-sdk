# Result

describes the output of a meta-analysis

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**meta_analysis_id** | **string** | the meta analysis this result was derived from. | [optional] [default to undefined]
**cli_version** | **string** | version of the command-line-tool that is uploading the results.  | [optional] [default to undefined]
**neurovault_collection** | [**NeurovaultCollectionReturn**](NeurovaultCollectionReturn.md) |  | [optional] [default to undefined]
**methods_description** | **string** | the description of the methods applied to create this result. | [optional] [default to undefined]
**diagnostic_table** | **string** | a text representation of a tsv that marks the contribution of each study to each particular cluster. | [optional] [default to undefined]
**cli_args** | **object** | additional parameters that were passed to the commandline tool at runtime.  | [optional] [default to undefined]
**status** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { Result } from './api';

const instance: Result = {
    meta_analysis_id,
    cli_version,
    neurovault_collection,
    methods_description,
    diagnostic_table,
    cli_args,
    status,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
