# SpecificationsApi

All URIs are relative to *https://compose.neurosynth.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**specificationsGet**](#specificationsget) | **GET** /specifications | Get a list of Specifications|
|[**specificationsIdGet**](#specificationsidget) | **GET** /specifications/{id} | Get information about a Specification|
|[**specificationsIdPut**](#specificationsidput) | **PUT** /specifications/{id} | Update Meta-Analysis specification|
|[**specificationsPost**](#specificationspost) | **POST** /specifications | Create a Specification|

# **specificationsGet**
> SpecificationList specificationsGet()

list of meta-analysis specifications

### Example

```typescript
import {
    SpecificationsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new SpecificationsApi(configuration);

let nested: boolean; //show nested component instead of id (optional) (default to undefined)
let ids: Array<string>; //choose the specific ids you wish to get (optional) (default to undefined)
let page: number; //page of results (optional) (default to undefined)
let pageSize: number; //number of elements to return on a page (optional) (default to undefined)
let search: string; //search for entries that contain the substring (optional) (default to undefined)
let sort: string; //Parameter to sort results on (optional) (default to 'created_at')
let desc: boolean; //sort results by descending order (as opposed to ascending order) (optional) (default to undefined)
let userId: string; //user id you want to filter on (optional) (default to undefined)
let info: boolean; //display additional information about a nested relationship without displaying fully nested object (optional) (default to undefined)

const { status, data } = await apiInstance.specificationsGet(
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

**SpecificationList**

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

# **specificationsIdGet**
> SpecificationReturn specificationsIdGet()

get a meta-analysis specification

### Example

```typescript
import {
    SpecificationsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new SpecificationsApi(configuration);

let id: string; // (default to undefined)

const { status, data } = await apiInstance.specificationsIdGet(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**SpecificationReturn**

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

# **specificationsIdPut**
> SpecificationReturn specificationsIdPut()

update an existing meta analysis specification

### Example

```typescript
import {
    SpecificationsApi,
    Configuration,
    Specification
} from './api';

const configuration = new Configuration();
const apiInstance = new SpecificationsApi(configuration);

let id: string; // (default to undefined)
let specification: Specification; // (optional)

const { status, data } = await apiInstance.specificationsIdPut(
    id,
    specification
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **specification** | **Specification**|  | |
| **id** | [**string**] |  | defaults to undefined|


### Return type

**SpecificationReturn**

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

# **specificationsPost**
> SpecificationReturn specificationsPost()

create a new meta-analysis specification

### Example

```typescript
import {
    SpecificationsApi,
    Configuration,
    SpecificationPostBody
} from './api';

const configuration = new Configuration();
const apiInstance = new SpecificationsApi(configuration);

let specificationPostBody: SpecificationPostBody; // (optional)

const { status, data } = await apiInstance.specificationsPost(
    specificationPostBody
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **specificationPostBody** | **SpecificationPostBody**|  | |


### Return type

**SpecificationReturn**

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
|**422** | Unprocessable Entity (WebDAV) |  -  |
|**500** | form when a request goes wrong |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

