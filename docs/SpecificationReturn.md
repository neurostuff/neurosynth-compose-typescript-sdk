# SpecificationReturn

The view of the specification through an endpoint.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | the type of meta-analysis being run, typically either cbma or ibma, but others may become available in the future. | [optional] [default to undefined]
**estimator** | [**Estimator**](Estimator.md) |  | [optional] [default to undefined]
**mask** | **string** | a string representing a binary nifti file to select which voxels a user wants to include in the analysis. | [optional] [default to undefined]
**conditions** | [**SpecificationConditions**](SpecificationConditions.md) |  | [optional] [default to undefined]
**weights** | **Array&lt;number&gt;** |  | [optional] [default to undefined]
**transformer** | **string** | A transformation applied to column(s) (e.g., binarize based on a threshold). This is likely to become deprecated. | [optional] [default to undefined]
**corrector** | [**Corrector**](Corrector.md) |  | [optional] [default to undefined]
**filter** | **string** | a column from annotations selecting which analyses to include in the meta-analysis | [optional] [default to undefined]
**database_studyset** | **string** |  | [optional] [default to undefined]
**id** | **string** | the identifier for the resource. | [optional] [default to undefined]
**updated_at** | **string** | when the resource was last modified. | [optional] [readonly] [default to undefined]
**created_at** | **string** | When the resource was created. | [optional] [readonly] [default to undefined]
**user** | **string** | Who owns the resource. | [optional] [default to undefined]
**username** | **string** |  | [optional] [readonly] [default to undefined]

## Example

```typescript
import { SpecificationReturn } from './api';

const instance: SpecificationReturn = {
    type,
    estimator,
    mask,
    conditions,
    weights,
    transformer,
    corrector,
    filter,
    database_studyset,
    id,
    updated_at,
    created_at,
    user,
    username,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
