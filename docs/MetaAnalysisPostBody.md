# MetaAnalysisPostBody


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**specification** | [**MetaAnalysisSpecification**](MetaAnalysisSpecification.md) |  | [optional] [default to undefined]
**studyset** | [**MetaAnalysisStudyset**](MetaAnalysisStudyset.md) |  | [optional] [default to undefined]
**annotation** | [**MetaAnalysisAnnotation**](MetaAnalysisAnnotation.md) |  | [optional] [default to undefined]
**name** | **string** | Human-readable name of the meta-analysis. | [optional] [default to undefined]
**description** | **string** | Long form description of the meta-analysis. | [optional] [default to undefined]
**tags** | [**MetaAnalysisTags**](MetaAnalysisTags.md) |  | [optional] [default to undefined]
**cached_studyset_id** | **string** | The id of the studyset on neurosynth-compose (as opposed to the id of the studyset on neurostore). Multiple snapshots of the studyset can be stored on neurosynth-compose so knowing which snapshot is being referenced is necessary. | [optional] [default to undefined]
**cached_annotation_id** | **string** | The id of the annotation on neurosynth-compose (as opposed to the id of the annotation on neurostore). Multiple snapshots of the annotation can be stored on neurosynth-compose so knowing which snapshot is being referenced is necessary. | [optional] [default to undefined]
**results** | [**MetaAnalysisResults**](MetaAnalysisResults.md) |  | [optional] [default to undefined]
**provenance** | **object** |  | [optional] [default to undefined]
**project** | **string** |  | [optional] [default to undefined]
**run_key** | **string** | a special key used to upload the results of this meta analysis. Can be used as an alternative to using your auth token from login.  | [optional] [readonly] [default to undefined]
**neurostore_analysis** | [**NeurostoreAnalysis**](NeurostoreAnalysis.md) |  | [optional] [default to undefined]
**cognitive_contrast_cogatlas** | **string** |  | [optional] [default to undefined]
**cognitive_contrast_cogatlas_id** | **string** |  | [optional] [default to undefined]
**cognitive_paradigm_cogatlas** | **string** |  | [optional] [default to undefined]
**cognitive_paradigm_cogatlas_id** | **string** |  | [optional] [default to undefined]
**cached_studyset** | **string** |  | [optional] [readonly] [default to undefined]
**cached_annotation** | **string** |  | [optional] [readonly] [default to undefined]
**neurostore_url** | **string** |  | [optional] [readonly] [default to undefined]

## Example

```typescript
import { MetaAnalysisPostBody } from './api';

const instance: MetaAnalysisPostBody = {
    specification,
    studyset,
    annotation,
    name,
    description,
    tags,
    cached_studyset_id,
    cached_annotation_id,
    results,
    provenance,
    project,
    run_key,
    neurostore_analysis,
    cognitive_contrast_cogatlas,
    cognitive_contrast_cogatlas_id,
    cognitive_paradigm_cogatlas,
    cognitive_paradigm_cogatlas_id,
    cached_studyset,
    cached_annotation,
    neurostore_url,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
