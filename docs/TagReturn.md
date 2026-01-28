# TagReturn


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Case-insensitive unique name within the tag scope (user or global). | [default to undefined]
**group** | **string** | Optional grouping key to categorize tags (case-insensitive exact match in queries). | [optional] [default to undefined]
**description** | **string** |  | [optional] [default to undefined]
**official** | **boolean** |  | [optional] [default to undefined]
**id** | **string** | the identifier for the resource. | [optional] [default to undefined]
**updated_at** | **string** | when the resource was last modified. | [optional] [readonly] [default to undefined]
**created_at** | **string** | When the resource was created. | [optional] [readonly] [default to undefined]
**user** | **string** | Who owns the resource. | [optional] [default to undefined]
**username** | **string** |  | [optional] [readonly] [default to undefined]

## Example

```typescript
import { TagReturn } from './api';

const instance: TagReturn = {
    name,
    group,
    description,
    official,
    id,
    updated_at,
    created_at,
    user,
    username,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
