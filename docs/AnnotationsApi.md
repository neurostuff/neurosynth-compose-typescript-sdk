# AnnotationsApi

All URIs are relative to *https://compose.neurosynth.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**annotationsGet**](#annotationsget) | **GET** /annotations | GET a list of annotations|
|[**annotationsIdGet**](#annotationsidget) | **GET** /annotations/{id} | GET information about an annotation|
|[**annotationsIdPut**](#annotationsidput) | **PUT** /annotations/{id} | Update an Annotation|
|[**annotationsPost**](#annotationspost) | **POST** /annotations | Create a new Annotation|

# **annotationsGet**
> AnnotationList annotationsGet()

get a list of serialized/referenced annotations

### Example

```typescript
import {
    AnnotationsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AnnotationsApi(configuration);

let nested: boolean; //show nested component instead of id (optional) (default to undefined)
let ids: Array<string>; //choose the specific ids you wish to get (optional) (default to undefined)
let page: number; //page of results (optional) (default to undefined)
let pageSize: number; //number of elements to return on a page (optional) (default to undefined)
let search: string; //search for entries that contain the substring (optional) (default to undefined)
let sort: string; //Parameter to sort results on (optional) (default to 'created_at')
let desc: boolean; //sort results by descending order (as opposed to ascending order) (optional) (default to undefined)
let userId: string; //user id you want to filter on (optional) (default to undefined)
let info: boolean; //display additional information about a nested relationship without displaying fully nested object (optional) (default to undefined)

const { status, data } = await apiInstance.annotationsGet(
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

**AnnotationList**

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

# **annotationsIdGet**
> AnnotationReturn annotationsIdGet()

get a single annotation

### Example

```typescript
import {
    AnnotationsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AnnotationsApi(configuration);

let id: string; // (default to undefined)

const { status, data } = await apiInstance.annotationsIdGet(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**AnnotationReturn**

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

# **annotationsIdPut**
> AnnotationReturn annotationsIdPut()

update an existing annotation

### Example

```typescript
import {
    AnnotationsApi,
    Configuration,
    AnnotationUpdate
} from './api';

const configuration = new Configuration();
const apiInstance = new AnnotationsApi(configuration);

let id: string; // (default to undefined)
let annotationUpdate: AnnotationUpdate; // (optional)

const { status, data } = await apiInstance.annotationsIdPut(
    id,
    annotationUpdate
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **annotationUpdate** | **AnnotationUpdate**|  | |
| **id** | [**string**] |  | defaults to undefined|


### Return type

**AnnotationReturn**

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
|**401** | form when a request goes wrong |  -  |
|**404** | form when a request goes wrong |  -  |
|**422** | form when a request goes wrong |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **annotationsPost**
> AnnotationReturn annotationsPost()

create a new serialized/referenced annotation

### Example

```typescript
import {
    AnnotationsApi,
    Configuration,
    AnnotationPostBody
} from './api';

const configuration = new Configuration();
const apiInstance = new AnnotationsApi(configuration);

let annotationPostBody: AnnotationPostBody; // (optional)

const { status, data } = await apiInstance.annotationsPost(
    annotationPostBody
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **annotationPostBody** | **AnnotationPostBody**|  | |


### Return type

**AnnotationReturn**

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

