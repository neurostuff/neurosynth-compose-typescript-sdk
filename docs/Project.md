# Project


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**provenance** | **object** |  | [optional] [default to undefined]
**meta_analyses** | [**ProjectMetaAnalyses**](ProjectMetaAnalyses.md) |  | [optional] [default to undefined]
**name** | **string** |  | [optional] [default to undefined]
**description** | **string** |  | [optional] [default to undefined]
**_public** | **boolean** | whether the project is public or private | [optional] [default to undefined]
**neurostore_study** | [**NeurostoreStudy**](NeurostoreStudy.md) |  | [optional] [default to undefined]
**neurostore_url** | **string** |  | [optional] [default to undefined]
**draft** | **boolean** |  | [optional] [readonly] [default to undefined]

## Example

```typescript
import { Project } from './api';

const instance: Project = {
    provenance,
    meta_analyses,
    name,
    description,
    _public,
    neurostore_study,
    neurostore_url,
    draft,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
