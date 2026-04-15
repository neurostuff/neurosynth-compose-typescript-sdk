# MetaAnalysisReturn


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**specification** | [**MetaAnalysisSpecification**](MetaAnalysisSpecification.md) |  | [optional] [default to undefined]
**neurostore_studyset** | [**MetaAnalysisNeurostoreStudyset**](MetaAnalysisNeurostoreStudyset.md) |  | [optional] [default to undefined]
**neurostore_annotation** | [**MetaAnalysisNeurostoreAnnotation**](MetaAnalysisNeurostoreAnnotation.md) |  | [optional] [default to undefined]
**name** | **string** | Human-readable name of the meta-analysis. | [optional] [default to undefined]
**description** | **string** | Long form description of the meta-analysis. | [optional] [default to undefined]
**_public** | **boolean** | whether the meta-analysis is public or private | [optional] [default to undefined]
**tags** | [**MetaAnalysisTags**](MetaAnalysisTags.md) |  | [optional] [default to undefined]
**results** | [**MetaAnalysisResults**](MetaAnalysisResults.md) |  | [optional] [default to undefined]
**provenance** | **object** |  | [optional] [default to undefined]
**project** | **string** |  | [optional] [default to undefined]
**run_key** | **string** | a special key used to upload the results of this meta analysis. Can be used as an alternative to using your auth token from login.  | [optional] [readonly] [default to undefined]
**snapshots** | **Array&lt;object&gt;** | Ordered history of (studyset, annotation) snapshot pairs recorded each time a MetaAnalysisResult is created. Each entry contains studyset_id, studyset_md5, annotation_id, annotation_md5, result_id, and created_at.  | [optional] [readonly] [default to undefined]
**neurostore_analysis** | [**NeurostoreAnalysis**](NeurostoreAnalysis.md) |  | [optional] [default to undefined]
**cognitive_contrast_cogatlas** | **string** |  | [optional] [default to undefined]
**cognitive_contrast_cogatlas_id** | **string** |  | [optional] [default to undefined]
**cognitive_paradigm_cogatlas** | **string** |  | [optional] [default to undefined]
**cognitive_paradigm_cogatlas_id** | **string** |  | [optional] [default to undefined]
**neurostore_url** | **string** |  | [optional] [readonly] [default to undefined]
**id** | **string** | the identifier for the resource. | [optional] [default to undefined]
**updated_at** | **string** | when the resource was last modified. | [optional] [readonly] [default to undefined]
**created_at** | **string** | When the resource was created. | [optional] [readonly] [default to undefined]
**user** | **string** | Who owns the resource. | [optional] [default to undefined]
**username** | **string** |  | [optional] [readonly] [default to undefined]

## Example

```typescript
import { MetaAnalysisReturn } from './api';

const instance: MetaAnalysisReturn = {
    specification,
    neurostore_studyset,
    neurostore_annotation,
    name,
    description,
    _public,
    tags,
    results,
    provenance,
    project,
    run_key,
    snapshots,
    neurostore_analysis,
    cognitive_contrast_cogatlas,
    cognitive_contrast_cogatlas_id,
    cognitive_paradigm_cogatlas,
    cognitive_paradigm_cogatlas_id,
    neurostore_url,
    id,
    updated_at,
    created_at,
    user,
    username,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
