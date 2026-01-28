# Tag

A user-scoped or global label that can be attached to multiple resources. Tag groups are free-form categories (e.g., \"visibility\", \"topic\") used to segment tags across different resource types.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Case-insensitive unique name within the tag scope (user or global). | [default to undefined]
**group** | **string** | Optional grouping key to categorize tags (case-insensitive exact match in queries). | [optional] [default to undefined]
**description** | **string** |  | [optional] [default to undefined]
**official** | **boolean** |  | [optional] [default to undefined]

## Example

```typescript
import { Tag } from './api';

const instance: Tag = {
    name,
    group,
    description,
    official,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
