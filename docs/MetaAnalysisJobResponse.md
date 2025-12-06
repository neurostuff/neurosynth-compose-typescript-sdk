# MetaAnalysisJobResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**job_id** | **string** | Identifier returned by the compose runner service. | [optional] [default to undefined]
**meta_analysis_id** | **string** | Identifier of the meta-analysis that was submitted. | [optional] [default to undefined]
**artifact_prefix** | **string** | Artifact key prefix for logs and outputs. | [optional] [default to undefined]
**status** | **string** | Latest known status reported by the compose runner. | [optional] [default to undefined]
**status_url** | **string** | Convenience URL for polling job status. | [optional] [default to undefined]
**environment** | **string** | Deployment environment the job was submitted to. | [optional] [default to undefined]
**no_upload** | **boolean** | Indicates whether the upload step was skipped. | [optional] [default to undefined]
**start_time** | **string** | Start time reported by the compose runner status endpoint. | [optional] [default to undefined]
**output** | **{ [key: string]: any; }** | Raw output payload returned by the compose runner. | [optional] [default to undefined]
**logs** | [**Array&lt;MetaAnalysisJobLog&gt;**](MetaAnalysisJobLog.md) | Aggregated log events returned by the compose runner. | [optional] [default to undefined]
**created_at** | **string** | Timestamp when the job entry was cached. | [optional] [default to undefined]
**updated_at** | **string** | Timestamp when the job entry was last refreshed. | [optional] [default to undefined]

## Example

```typescript
import { MetaAnalysisJobResponse } from './api';

const instance: MetaAnalysisJobResponse = {
    job_id,
    meta_analysis_id,
    artifact_prefix,
    status,
    status_url,
    environment,
    no_upload,
    start_time,
    output,
    logs,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
