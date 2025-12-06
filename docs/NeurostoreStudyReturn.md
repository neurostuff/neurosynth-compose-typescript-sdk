# NeurostoreStudyReturn


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**neurostore_id** | **string** |  | [optional] [readonly] [default to undefined]
**analyses** | [**Array&lt;NeurostoreAnalysis&gt;**](NeurostoreAnalysis.md) |  | [optional] [default to undefined]
**exception** | **string** |  | [optional] [default to undefined]
**traceback** | **string** |  | [optional] [default to undefined]
**status** | **string** |  | [optional] [default to undefined]
**id** | **string** | the identifier for the resource. | [optional] [default to undefined]
**updated_at** | **string** | when the resource was last modified. | [optional] [readonly] [default to undefined]
**created_at** | **string** | When the resource was created. | [optional] [readonly] [default to undefined]
**user** | **string** | Who owns the resource. | [optional] [default to undefined]
**username** | **string** |  | [optional] [readonly] [default to undefined]

## Example

```typescript
import { NeurostoreStudyReturn } from './api';

const instance: NeurostoreStudyReturn = {
    neurostore_id,
    analyses,
    exception,
    traceback,
    status,
    id,
    updated_at,
    created_at,
    user,
    username,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
