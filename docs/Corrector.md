# Corrector

The function/class applying statistical adjustments to the output of the meta-analysis (optional).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | the name of the function/class performing the correction. For example FWECorrector from NiMARE would be valid. | [optional] [default to undefined]
**args** | **object** | key word arguments passed to the corrector to modidy default functionality, such as number of iterations, or the particular method of correction being applied. | [optional] [default to undefined]

## Example

```typescript
import { Corrector } from './api';

const instance: Corrector = {
    type,
    args,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
