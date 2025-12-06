# GetApi

All URIs are relative to *https://compose.neurosynth.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**annotationsGet**](#annotationsget) | **GET** /annotations | GET a list of annotations|
|[**annotationsIdGet**](#annotationsidget) | **GET** /annotations/{id} | GET information about an annotation|
|[**metaAnalysesGet**](#metaanalysesget) | **GET** /meta-analyses | GET a list of meta-analyses|
|[**metaAnalysesIdGet**](#metaanalysesidget) | **GET** /meta-analyses/{id} | GET meta-analysis information|
|[**metaAnalysisResultsGet**](#metaanalysisresultsget) | **GET** /meta-analysis-results | Your GET endpoint|
|[**metaAnalysisResultsIdGet**](#metaanalysisresultsidget) | **GET** /meta-analysis-results/{id} | Your GET endpoint|
|[**neurosynthComposeResourcesMetaAnalysisJobsMetaAnalysisJobResourceGet**](#neurosynthcomposeresourcesmetaanalysisjobsmetaanalysisjobresourceget) | **GET** /meta-analysis-jobs/{job_id} | Get status and logs for a meta-analysis job|
|[**neurosynthComposeResourcesMetaAnalysisJobsMetaAnalysisJobsResourceGet**](#neurosynthcomposeresourcesmetaanalysisjobsmetaanalysisjobsresourceget) | **GET** /meta-analysis-jobs | List meta-analysis jobs for the current user|
|[**projectsGet**](#projectsget) | **GET** /projects | Your GET endpoint|
|[**projectsIdGet**](#projectsidget) | **GET** /projects/{id} | Your GET endpoint|
|[**specificationsGet**](#specificationsget) | **GET** /specifications | Get a list of Specifications|
|[**specificationsIdGet**](#specificationsidget) | **GET** /specifications/{id} | Get information about a Specification|
|[**studysetsGet**](#studysetsget) | **GET** /studysets | Get a list of Studysets|
|[**studysetsIdGet**](#studysetsidget) | **GET** /studysets/{id} | Get information about a Studyset|

# **annotationsGet**
> AnnotationList annotationsGet()

get a list of serialized/referenced annotations

### Example

```typescript
import {
    GetApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new GetApi(configuration);

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
    GetApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new GetApi(configuration);

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

# **metaAnalysesGet**
> MetaAnalysisList metaAnalysesGet()

list all runnable specification, studyset, annotation bundles

### Example

```typescript
import {
    GetApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new GetApi(configuration);

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

# **metaAnalysesIdGet**
> MetaAnalysisReturn metaAnalysesIdGet()

get a meta-analysis (specification, annotation, and studyset)

### Example

```typescript
import {
    GetApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new GetApi(configuration);

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

# **metaAnalysisResultsGet**
> ResultList metaAnalysisResultsGet()


### Example

```typescript
import {
    GetApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new GetApi(configuration);

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
    GetApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new GetApi(configuration);

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

# **neurosynthComposeResourcesMetaAnalysisJobsMetaAnalysisJobResourceGet**
> MetaAnalysisJobResponse neurosynthComposeResourcesMetaAnalysisJobsMetaAnalysisJobResourceGet()

Retrieve the most recent status information and logs for a submitted job.

### Example

```typescript
import {
    GetApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new GetApi(configuration);

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
    GetApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new GetApi(configuration);

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

# **projectsGet**
> ProjectList projectsGet()


### Example

```typescript
import {
    GetApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new GetApi(configuration);

let page: number; //page of results (optional) (default to undefined)
let pageSize: number; //number of elements to return on a page (optional) (default to undefined)
let name: string; //search the name field for a term (optional) (default to undefined)
let search: string; //search for entries that contain the substring (optional) (default to undefined)
let description: string; //search description field for a term (optional) (default to undefined)
let sort: string; //Parameter to sort results on (optional) (default to 'created_at')
let desc: boolean; //sort results by descending order (as opposed to ascending order) (optional) (default to undefined)
let userId: string; //user id you want to filter on (optional) (default to undefined)

const { status, data } = await apiInstance.projectsGet(
    page,
    pageSize,
    name,
    search,
    description,
    sort,
    desc,
    userId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **page** | [**number**] | page of results | (optional) defaults to undefined|
| **pageSize** | [**number**] | number of elements to return on a page | (optional) defaults to undefined|
| **name** | [**string**] | search the name field for a term | (optional) defaults to undefined|
| **search** | [**string**] | search for entries that contain the substring | (optional) defaults to undefined|
| **description** | [**string**] | search description field for a term | (optional) defaults to undefined|
| **sort** | [**string**] | Parameter to sort results on | (optional) defaults to 'created_at'|
| **desc** | [**boolean**] | sort results by descending order (as opposed to ascending order) | (optional) defaults to undefined|
| **userId** | [**string**] | user id you want to filter on | (optional) defaults to undefined|


### Return type

**ProjectList**

### Authorization

[JSON-Web-Token](../README.md#JSON-Web-Token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **projectsIdGet**
> ProjectReturn projectsIdGet()


### Example

```typescript
import {
    GetApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new GetApi(configuration);

let id: string; // (default to undefined)
let info: boolean; //display additional information about a nested relationship without displaying fully nested object (optional) (default to undefined)

const { status, data } = await apiInstance.projectsIdGet(
    id,
    info
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] |  | defaults to undefined|
| **info** | [**boolean**] | display additional information about a nested relationship without displaying fully nested object | (optional) defaults to undefined|


### Return type

**ProjectReturn**

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

# **specificationsGet**
> SpecificationList specificationsGet()

list of meta-analysis specifications

### Example

```typescript
import {
    GetApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new GetApi(configuration);

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
    GetApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new GetApi(configuration);

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

# **studysetsGet**
> StudysetList studysetsGet()

get a list of serialized/referenced studysets

### Example

```typescript
import {
    GetApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new GetApi(configuration);

let nested: boolean; //show nested component instead of id (optional) (default to undefined)
let ids: Array<string>; //choose the specific ids you wish to get (optional) (default to undefined)
let page: number; //page of results (optional) (default to undefined)
let pageSize: number; //number of elements to return on a page (optional) (default to undefined)
let search: string; //search for entries that contain the substring (optional) (default to undefined)
let sort: string; //Parameter to sort results on (optional) (default to 'created_at')
let desc: boolean; //sort results by descending order (as opposed to ascending order) (optional) (default to undefined)
let userId: string; //user id you want to filter on (optional) (default to undefined)
let info: boolean; //display additional information about a nested relationship without displaying fully nested object (optional) (default to undefined)

const { status, data } = await apiInstance.studysetsGet(
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

# **studysetsIdGet**
> StudysetReturn studysetsIdGet()

get a single serialized/referenced studyset

### Example

```typescript
import {
    GetApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new GetApi(configuration);

let id: string; // (default to undefined)

const { status, data } = await apiInstance.studysetsIdGet(
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

