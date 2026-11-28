# CurationChangeset

Stub changes applied together. A stub is named by its `id`. `index` is the place in the target column after the earlier changes in this changeset; 0 is the top and a negative index counts from the bottom (-1 is the last place). Added stubs without an `index` go to the top of their column in the order given.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**updated_at** | **string** | the project\&#39;s &#x60;updated_at&#x60; the client last saw; a project that has changed since is refused with 409 | [optional] [default to undefined]
**remove** | **Array&lt;string&gt;** | ids of stubs to delete | [optional] [default to undefined]
**add** | [**Array&lt;CurationChangesetAddInner&gt;**](CurationChangesetAddInner.md) |  | [optional] [default to undefined]
**update** | [**Array&lt;CurationStub&gt;**](CurationStub.md) | each item names a stub by &#x60;id&#x60;; its other keys replace that stub\&#39;s keys | [optional] [default to undefined]
**move** | [**Array&lt;CurationChangesetMoveInner&gt;**](CurationChangesetMoveInner.md) |  | [optional] [default to undefined]

## Example

```typescript
import { CurationChangeset } from './api';

const instance: CurationChangeset = {
    updated_at,
    remove,
    add,
    update,
    move,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
