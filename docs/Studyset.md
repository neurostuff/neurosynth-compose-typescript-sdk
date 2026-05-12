# Studyset


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**neurostore_id** | **string** | The id of the studyset on neurostore. | [optional] [default to undefined]
**snapshot** | **object** | The snapshot of the studyset pending a successful run of the meta-analysis. | [optional] [default to undefined]
**neurostore_url** | **string** |  | [optional] [readonly] [default to undefined]
**version** | **string** | A string representing a labeled version of this particular studyset. | [optional] [default to undefined]

## Example

```typescript
import { Studyset } from './api';

const instance: Studyset = {
    neurostore_id,
    snapshot,
    neurostore_url,
    version,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
