# CurationSummaryColumnsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [default to undefined]
**name** | **string** |  | [optional] [default to undefined]
**stub_count** | **number** |  | [optional] [default to undefined]
**exclusions** | **{ [key: string]: number; }** | stub count per exclusion tag id | [optional] [default to undefined]
**tags** | **{ [key: string]: number; }** | stub count per tag id | [optional] [default to undefined]

## Example

```typescript
import { CurationSummaryColumnsInner } from './api';

const instance: CurationSummaryColumnsInner = {
    id,
    name,
    stub_count,
    exclusions,
    tags,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
