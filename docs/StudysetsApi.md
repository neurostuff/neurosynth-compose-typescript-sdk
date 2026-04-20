# StudysetsApi

All URIs are relative to *https://compose.neurosynth.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**snapshotStudysetsGet**](#snapshotstudysetsget) | **GET** /snapshot-studysets | Get a list of Studysets|
|[**snapshotStudysetsIdGet**](#snapshotstudysetsidget) | **GET** /snapshot-studysets/{id} | Get information about a Studyset|
|[**snapshotStudysetsIdPut**](#snapshotstudysetsidput) | **PUT** /snapshot-studysets/{id} | Update a Studyset|
|[**snapshotStudysetsPost**](#snapshotstudysetspost) | **POST** /snapshot-studysets | Create a new Studyset|

# **snapshotStudysetsGet**
> StudysetList snapshotStudysetsGet()

get a list of serialized/referenced studysets

### Example

```typescript
import {
    StudysetsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new StudysetsApi(configuration);

let nested: boolean; //show nested component instead of id (optional) (default to undefined)
let ids: Array<string>; //choose the specific ids you wish to get (optional) (default to undefined)
let page: number; //page of results (optional) (default to undefined)
let pageSize: number; //number of elements to return on a page (optional) (default to undefined)
let search: string; //search for entries that contain the substring (optional) (default to undefined)
let sort: string; //Parameter to sort results on (optional) (default to 'created_at')
let desc: boolean; //sort results by descending order (as opposed to ascending order) (optional) (default to undefined)
let userId: string; //user id you want to filter on (optional) (default to undefined)
let info: boolean; //display additional information about a nested relationship without displaying fully nested object (optional) (default to undefined)

const { status, data } = await apiInstance.snapshotStudysetsGet(
    nested,
    ids,
    page,
    pageSize,
    search,
    sort,
    desc,
    userId,
    info
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **nested** | [**boolean**] | show nested component instead of id | (optional) defaults to undefined|
| **ids** | **Array&lt;string&gt;** | choose the specific ids you wish to get | (optional) defaults to undefined|
| **page** | [**number**] | page of results | (optional) defaults to undefined|
| **pageSize** | [**number**] | number of elements to return on a page | (optional) defaults to undefined|
| **search** | [**string**] | search for entries that contain the substring | (optional) defaults to undefined|
| **sort** | [**string**] | Parameter to sort results on | (optional) defaults to 'created_at'|
| **desc** | [**boolean**] | sort results by descending order (as opposed to ascending order) | (optional) defaults to undefined|
| **userId** | [**string**] | user id you want to filter on | (optional) defaults to undefined|
| **info** | [**boolean**] | display additional information about a nested relationship without displaying fully nested object | (optional) defaults to undefined|


### Return type

**StudysetList**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |
|**400** | form when a request goes wrong |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **snapshotStudysetsIdGet**
> StudysetReturn snapshotStudysetsIdGet()

get a single serialized/referenced studyset

### Example

```typescript
import {
    StudysetsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new StudysetsApi(configuration);

let id: string; // (default to undefined)

const { status, data } = await apiInstance.snapshotStudysetsIdGet(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**StudysetReturn**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |
|**401** | form when a request goes wrong |  -  |
|**404** | form when a request goes wrong |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **snapshotStudysetsIdPut**
> StudysetReturn snapshotStudysetsIdPut()

update an existing serialized/referenced studyset

### Example

```typescript
import {
    StudysetsApi,
    Configuration,
    Studyset
} from './api';

const configuration = new Configuration();
const apiInstance = new StudysetsApi(configuration);

let id: string; // (default to undefined)
let studyset: Studyset; // (optional)

const { status, data } = await apiInstance.snapshotStudysetsIdPut(
    id,
    studyset
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **studyset** | **Studyset**|  | |
| **id** | [**string**] |  | defaults to undefined|


### Return type

**StudysetReturn**

### Authorization

[JSON-Web-Token](../README.md#JSON-Web-Token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |
|**400** | Bad Request |  -  |
|**401** | form when a request goes wrong |  -  |
|**404** | form when a request goes wrong |  -  |
|**422** | form when a request goes wrong |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **snapshotStudysetsPost**
> StudysetReturn snapshotStudysetsPost()

create a new serialized/referenced studyset

### Example

```typescript
import {
    StudysetsApi,
    Configuration,
    StudysetPostBody
} from './api';

const configuration = new Configuration();
const apiInstance = new StudysetsApi(configuration);

let studysetPostBody: StudysetPostBody; // (optional)

const { status, data } = await apiInstance.snapshotStudysetsPost(
    studysetPostBody
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **studysetPostBody** | **StudysetPostBody**|  | |


### Return type

**StudysetReturn**

### Authorization

[JSON-Web-Token](../README.md#JSON-Web-Token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |
|**400** | form when a request goes wrong |  -  |
|**422** | form when a request goes wrong |  -  |
|**500** | form when a request goes wrong |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

