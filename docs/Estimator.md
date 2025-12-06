# Estimator

the specification for the function/class running the meta-analysis

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | the meta-analytic algorithm applied to the data. Currently this should be directly tied to the function/class running the meta-analysis. For example, ALE, or MKDADensity are valid NiMARE classes to put here. | [optional] [default to undefined]
**args** | **object** | arbitrary keyword arguments to be passed into the function/class to modify default functionality, this could modify the kernel, resampling methods, or any other behavior defined in the function/class (like MKDADensity). | [optional] [default to undefined]

## Example

```typescript
import { Estimator } from './api';

const instance: Estimator = {
    type,
    args,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
