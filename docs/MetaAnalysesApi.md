# MetaAnalysesApi

All URIs are relative to *https://compose.neurosynth.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**metaAnalysesGet**](#metaanalysesget) | **GET** /meta-analyses | GET a list of meta-analyses|
|[**metaAnalysesIdGet**](#metaanalysesidget) | **GET** /meta-analyses/{id} | GET meta-analysis information|
|[**metaAnalysesIdPut**](#metaanalysesidput) | **PUT** /meta-analyses/{id} | Update a meta-analysis|
|[**metaAnalysesPost**](#metaanalysespost) | **POST** /meta-analyses | Create a new meta-analysis|
|[**metaAnalysisResultsGet**](#metaanalysisresultsget) | **GET** /meta-analysis-results | Your GET endpoint|
|[**metaAnalysisResultsIdGet**](#metaanalysisresultsidget) | **GET** /meta-analysis-results/{id} | Your GET endpoint|
|[**metaAnalysisResultsIdPut**](#metaanalysisresultsidput) | **PUT** /meta-analysis-results/{id} | |
|[**metaAnalysisResultsPost**](#metaanalysisresultspost) | **POST** /meta-analysis-results | |
|[**neurosynthComposeResourcesMetaAnalysisJobsMetaAnalysisJobResourceGet**](#neurosynthcomposeresourcesmetaanalysisjobsmetaanalysisjobresourceget) | **GET** /meta-analysis-jobs/{job_id} | Get status and logs for a meta-analysis job|
|[**neurosynthComposeResourcesMetaAnalysisJobsMetaAnalysisJobsResourceGet**](#neurosynthcomposeresourcesmetaanalysisjobsmetaanalysisjobsresourceget) | **GET** /meta-analysis-jobs | List meta-analysis jobs for the current user|
|[**neurosynthComposeResourcesMetaAnalysisJobsMetaAnalysisJobsResourcePost**](#neurosynthcomposeresourcesmetaanalysisjobsmetaanalysisjobsresourcepost) | **POST** /meta-analysis-jobs | Submit a meta-analysis job|

# **metaAnalysesGet**
> MetaAnalysisList metaAnalysesGet()

list all runnable specification, studyset, annotation bundles

### Example

```typescript
import {
    MetaAnalysesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MetaAnalysesApi(configuration);

let nested: boolean; //show nested component instead of id (optional) (default to undefined)
let ids: Array<string>; //choose the specific ids you wish to get (optional) (default to undefined)
let page: number; //page of results (optional) (default to undefined)
let pageSize: number; //number of elements to return on a page (optional) (default to undefined)
let name: string; //search the name field for a term (optional) (default to undefined)
let search: string; //search for entries that contain the substring (optional) (default to undefined)
let description: string; //search description field for a term (optional) (default to undefined)
let sort: string; //Parameter to sort results on (optional) (default to 'created_at')
let desc: boolean; //sort results by descending order (as opposed to ascending order) (optional) (default to undefined)

const { status, data } = await apiInstance.metaAnalysesGet(
    nested,
    ids,
    page,
    pageSize,
    name,
    search,
    description,
    sort,
    desc
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **nested** | [**boolean**] | show nested component instead of id | (optional) defaults to undefined|
| **ids** | **Array&lt;string&gt;** | choose the specific ids you wish to get | (optional) defaults to undefined|
| **page** | [**number**] | page of results | (optional) defaults to undefined|
| **pageSize** | [**number**] | number of elements to return on a page | (optional) defaults to undefined|
| **name** | [**string**] | search the name field for a term | (optional) defaults to undefined|
| **search** | [**string**] | search for entries that contain the substring | (optional) defaults to undefined|
| **description** | [**string**] | search description field for a term | (optional) defaults to undefined|
| **sort** | [**string**] | Parameter to sort results on | (optional) defaults to 'created_at'|
| **desc** | [**boolean**] | sort results by descending order (as opposed to ascending order) | (optional) defaults to undefined|


### Return type

**MetaAnalysisList**

### Authorization

[JSON-Web-Token](../README.md#JSON-Web-Token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |
|**400** | form when a request goes wrong |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **metaAnalysesIdGet**
> MetaAnalysisReturn metaAnalysesIdGet()

get a meta-analysis (specification, annotation, and studyset)

### Example

```typescript
import {
    MetaAnalysesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MetaAnalysesApi(configuration);

let id: string; // (default to undefined)
let nested: boolean; //show nested component instead of id (optional) (default to undefined)

const { status, data } = await apiInstance.metaAnalysesIdGet(
    id,
    nested
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] |  | defaults to undefined|
| **nested** | [**boolean**] | show nested component instead of id | (optional) defaults to undefined|


### Return type

**MetaAnalysisReturn**

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

# **metaAnalysesIdPut**
> MetaAnalysisReturn metaAnalysesIdPut()

update an existing meta-analysis (that has not yet been run)

### Example

```typescript
import {
    MetaAnalysesApi,
    Configuration,
    MetaAnalysis
} from './api';

const configuration = new Configuration();
const apiInstance = new MetaAnalysesApi(configuration);

let id: string; // (default to undefined)
let metaAnalysis: MetaAnalysis; // (optional)

const { status, data } = await apiInstance.metaAnalysesIdPut(
    id,
    metaAnalysis
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **metaAnalysis** | **MetaAnalysis**|  | |
| **id** | [**string**] |  | defaults to undefined|


### Return type

**MetaAnalysisReturn**

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

# **metaAnalysesPost**
> MetaAnalysisReturn metaAnalysesPost()

create a new specification, studyset, annotation bundle

### Example

```typescript
import {
    MetaAnalysesApi,
    Configuration,
    MetaAnalysisPostBody
} from './api';

const configuration = new Configuration();
const apiInstance = new MetaAnalysesApi(configuration);

let metaAnalysisPostBody: MetaAnalysisPostBody; // (optional)

const { status, data } = await apiInstance.metaAnalysesPost(
    metaAnalysisPostBody
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **metaAnalysisPostBody** | **MetaAnalysisPostBody**|  | |


### Return type

**MetaAnalysisReturn**

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

# **metaAnalysisResultsGet**
> ResultList metaAnalysisResultsGet()


### Example

```typescript
import {
    MetaAnalysesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MetaAnalysesApi(configuration);

let metaAnalysisId: string; //search for results with this meta-analysis id (optional) (default to undefined)

const { status, data } = await apiInstance.metaAnalysisResultsGet(
    metaAnalysisId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **metaAnalysisId** | [**string**] | search for results with this meta-analysis id | (optional) defaults to undefined|


### Return type

**ResultList**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **metaAnalysisResultsIdGet**
> ResultReturn metaAnalysisResultsIdGet()


### Example

```typescript
import {
    MetaAnalysesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MetaAnalysesApi(configuration);

let id: string; // (default to undefined)

const { status, data } = await apiInstance.metaAnalysisResultsIdGet(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**ResultReturn**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **metaAnalysisResultsIdPut**
> ResultReturn metaAnalysisResultsIdPut()


### Example

```typescript
import {
    MetaAnalysesApi,
    Configuration,
    Result
} from './api';

const configuration = new Configuration();
const apiInstance = new MetaAnalysesApi(configuration);

let id: string; // (default to undefined)
let result: Result; // (optional)

const { status, data } = await apiInstance.metaAnalysisResultsIdPut(
    id,
    result
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **result** | **Result**|  | |
| **id** | [**string**] |  | defaults to undefined|


### Return type

**ResultReturn**

### Authorization

[JSON-Web-Token](../README.md#JSON-Web-Token), [upload_key](../README.md#upload_key)

### HTTP request headers

 - **Content-Type**: application/json, multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **metaAnalysisResultsPost**
> ResultReturn metaAnalysisResultsPost()


### Example

```typescript
import {
    MetaAnalysesApi,
    Configuration,
    ResultInit
} from './api';

const configuration = new Configuration();
const apiInstance = new MetaAnalysesApi(configuration);

let resultInit: ResultInit; // (optional)

const { status, data } = await apiInstance.metaAnalysisResultsPost(
    resultInit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **resultInit** | **ResultInit**|  | |


### Return type

**ResultReturn**

### Authorization

[JSON-Web-Token](../README.md#JSON-Web-Token), [upload_key](../README.md#upload_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **neurosynthComposeResourcesMetaAnalysisJobsMetaAnalysisJobResourceGet**
> MetaAnalysisJobResponse neurosynthComposeResourcesMetaAnalysisJobsMetaAnalysisJobResourceGet()

Retrieve the most recent status information and logs for a submitted job.

### Example

```typescript
import {
    MetaAnalysesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MetaAnalysesApi(configuration);

let jobId: string; // (default to undefined)

const { status, data } = await apiInstance.neurosynthComposeResourcesMetaAnalysisJobsMetaAnalysisJobResourceGet(
    jobId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **jobId** | [**string**] |  | defaults to undefined|


### Return type

**MetaAnalysisJobResponse**

### Authorization

[JSON-Web-Token](../README.md#JSON-Web-Token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |
|**401** | form when a request goes wrong |  -  |
|**404** | form when a request goes wrong |  -  |
|**502** | form when a request goes wrong |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **neurosynthComposeResourcesMetaAnalysisJobsMetaAnalysisJobsResourceGet**
> MetaAnalysisJobList neurosynthComposeResourcesMetaAnalysisJobsMetaAnalysisJobsResourceGet()

Return cached job submissions associated with the authenticated user.

### Example

```typescript
import {
    MetaAnalysesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MetaAnalysesApi(configuration);

const { status, data } = await apiInstance.neurosynthComposeResourcesMetaAnalysisJobsMetaAnalysisJobsResourceGet();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**MetaAnalysisJobList**

### Authorization

[JSON-Web-Token](../README.md#JSON-Web-Token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |
|**401** | form when a request goes wrong |  -  |
|**502** | form when a request goes wrong |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **neurosynthComposeResourcesMetaAnalysisJobsMetaAnalysisJobsResourcePost**
> MetaAnalysisJobResponse neurosynthComposeResourcesMetaAnalysisJobsMetaAnalysisJobsResourcePost(metaAnalysisJobRequest)

Submit a meta-analysis to the compose runner service.

### Example

```typescript
import {
    MetaAnalysesApi,
    Configuration,
    MetaAnalysisJobRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new MetaAnalysesApi(configuration);

let metaAnalysisJobRequest: MetaAnalysisJobRequest; //

const { status, data } = await apiInstance.neurosynthComposeResourcesMetaAnalysisJobsMetaAnalysisJobsResourcePost(
    metaAnalysisJobRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **metaAnalysisJobRequest** | **MetaAnalysisJobRequest**|  | |


### Return type

**MetaAnalysisJobResponse**

### Authorization

[JSON-Web-Token](../README.md#JSON-Web-Token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**202** | Job accepted |  -  |
|**401** | form when a request goes wrong |  -  |
|**403** | form when a request goes wrong |  -  |
|**422** | form when a request goes wrong |  -  |
|**502** | form when a request goes wrong |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

