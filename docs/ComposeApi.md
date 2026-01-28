# ComposeApi

All URIs are relative to *https://compose.neurosynth.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**annotationsGet**](#annotationsget) | **GET** /annotations | GET a list of annotations|
|[**annotationsIdGet**](#annotationsidget) | **GET** /annotations/{id} | GET information about an annotation|
|[**annotationsIdPut**](#annotationsidput) | **PUT** /annotations/{id} | Update an Annotation|
|[**annotationsPost**](#annotationspost) | **POST** /annotations | Create a new Annotation|
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
|[**projectsGet**](#projectsget) | **GET** /projects | Your GET endpoint|
|[**projectsIdDelete**](#projectsiddelete) | **DELETE** /projects/{id} | |
|[**projectsIdGet**](#projectsidget) | **GET** /projects/{id} | Your GET endpoint|
|[**projectsIdPut**](#projectsidput) | **PUT** /projects/{id} | |
|[**projectsPost**](#projectspost) | **POST** /projects | |
|[**specificationsGet**](#specificationsget) | **GET** /specifications | Get a list of Specifications|
|[**specificationsIdGet**](#specificationsidget) | **GET** /specifications/{id} | Get information about a Specification|
|[**specificationsIdPut**](#specificationsidput) | **PUT** /specifications/{id} | Update Meta-Analysis specification|
|[**specificationsPost**](#specificationspost) | **POST** /specifications | Create a Specification|
|[**studysetsGet**](#studysetsget) | **GET** /studysets | Get a list of Studysets|
|[**studysetsIdGet**](#studysetsidget) | **GET** /studysets/{id} | Get information about a Studyset|
|[**studysetsIdPut**](#studysetsidput) | **PUT** /studysets/{id} | Update a Studyset|
|[**studysetsPost**](#studysetspost) | **POST** /studysets | Create a new Studyset|
|[**tagsGet**](#tagsget) | **GET** /tags | Get a list of Tags|
|[**tagsIdGet**](#tagsidget) | **GET** /tags/{id} | Get information about a Tag|
|[**tagsPost**](#tagspost) | **POST** /tags | Create a new Tag|

# **annotationsGet**
> AnnotationList annotationsGet()

get a list of serialized/referenced annotations

### Example

```typescript
import {
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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
    ComposeApi,
    Configuration,
    AnnotationUpdate
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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
    ComposeApi,
    Configuration,
    AnnotationPostBody
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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

# **metaAnalysesGet**
> MetaAnalysisList metaAnalysesGet()

list all runnable specification, studyset, annotation bundles

### Example

```typescript
import {
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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
    ComposeApi,
    Configuration,
    MetaAnalysis
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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
    ComposeApi,
    Configuration,
    MetaAnalysisPostBody
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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
    ComposeApi,
    Configuration,
    Result
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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
    ComposeApi,
    Configuration,
    ResultInit
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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
    ComposeApi,
    Configuration,
    MetaAnalysisJobRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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

# **projectsGet**
> ProjectList projectsGet()


### Example

```typescript
import {
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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

# **projectsIdDelete**
> projectsIdDelete()


### Example

```typescript
import {
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

let id: string; // (default to undefined)

const { status, data } = await apiInstance.projectsIdDelete(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] |  | defaults to undefined|


### Return type

void (empty response body)

### Authorization

[JSON-Web-Token](../README.md#JSON-Web-Token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**204** | No Content |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **projectsIdGet**
> ProjectReturn projectsIdGet()


### Example

```typescript
import {
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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

# **projectsIdPut**
> ProjectReturn projectsIdPut()


### Example

```typescript
import {
    ComposeApi,
    Configuration,
    Project
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

let id: string; // (default to undefined)
let project: Project; // (optional)

const { status, data } = await apiInstance.projectsIdPut(
    id,
    project
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **project** | **Project**|  | |
| **id** | [**string**] |  | defaults to undefined|


### Return type

**ProjectReturn**

### Authorization

[JSON-Web-Token](../README.md#JSON-Web-Token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **projectsPost**
> ProjectReturn projectsPost()


### Example

```typescript
import {
    ComposeApi,
    Configuration,
    Project
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

let sourceId: string; //clone an existing project when creating a new project (optional) (default to undefined)
let copyAnnotations: boolean; //when cloning via `source_id`, also duplicate associated annotations (optional) (default to undefined)
let project: Project; // (optional)

const { status, data } = await apiInstance.projectsPost(
    sourceId,
    copyAnnotations,
    project
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **project** | **Project**|  | |
| **sourceId** | [**string**] | clone an existing project when creating a new project | (optional) defaults to undefined|
| **copyAnnotations** | [**boolean**] | when cloning via &#x60;source_id&#x60;, also duplicate associated annotations | (optional) defaults to undefined|


### Return type

**ProjectReturn**

### Authorization

[JSON-Web-Token](../README.md#JSON-Web-Token)

### HTTP request headers

 - **Content-Type**: application/json
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
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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
    ComposeApi,
    Configuration,
    Specification
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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
    ComposeApi,
    Configuration,
    SpecificationPostBody
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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

# **studysetsGet**
> StudysetList studysetsGet()

get a list of serialized/referenced studysets

### Example

```typescript
import {
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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

# **studysetsIdPut**
> StudysetReturn studysetsIdPut()

update an existing serialized/referenced studyset

### Example

```typescript
import {
    ComposeApi,
    Configuration,
    Studyset
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

let id: string; // (default to undefined)
let studyset: Studyset; // (optional)

const { status, data } = await apiInstance.studysetsIdPut(
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

# **studysetsPost**
> StudysetReturn studysetsPost()

create a new serialized/referenced studyset

### Example

```typescript
import {
    ComposeApi,
    Configuration,
    StudysetPostBody
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

let studysetPostBody: StudysetPostBody; // (optional)

const { status, data } = await apiInstance.studysetsPost(
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

# **tagsGet**
> TagList tagsGet()


### Example

```typescript
import {
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

let ids: Array<string>; //choose the specific ids you wish to get (optional) (default to undefined)
let page: number; //page of results (optional) (default to undefined)
let pageSize: number; //number of elements to return on a page (optional) (default to undefined)
let name: string; //search the name field for a term (optional) (default to undefined)
let search: string; //search for entries that contain the substring (optional) (default to undefined)
let filter: string; //alias for search when filtering tags (optional) (default to undefined)
let description: string; //search description field for a term (optional) (default to undefined)
let group: string; //filter tags by group (optional) (default to undefined)
let official: boolean; //filter tags by official flag (optional) (default to undefined)
let sort: string; //Parameter to sort results on (optional) (default to 'created_at')
let desc: boolean; //sort results by descending order (as opposed to ascending order) (optional) (default to undefined)
let userId: string; //user id you want to filter on (optional) (default to undefined)

const { status, data } = await apiInstance.tagsGet(
    ids,
    page,
    pageSize,
    name,
    search,
    filter,
    description,
    group,
    official,
    sort,
    desc,
    userId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **ids** | **Array&lt;string&gt;** | choose the specific ids you wish to get | (optional) defaults to undefined|
| **page** | [**number**] | page of results | (optional) defaults to undefined|
| **pageSize** | [**number**] | number of elements to return on a page | (optional) defaults to undefined|
| **name** | [**string**] | search the name field for a term | (optional) defaults to undefined|
| **search** | [**string**] | search for entries that contain the substring | (optional) defaults to undefined|
| **filter** | [**string**] | alias for search when filtering tags | (optional) defaults to undefined|
| **description** | [**string**] | search description field for a term | (optional) defaults to undefined|
| **group** | [**string**] | filter tags by group | (optional) defaults to undefined|
| **official** | [**boolean**] | filter tags by official flag | (optional) defaults to undefined|
| **sort** | [**string**] | Parameter to sort results on | (optional) defaults to 'created_at'|
| **desc** | [**boolean**] | sort results by descending order (as opposed to ascending order) | (optional) defaults to undefined|
| **userId** | [**string**] | user id you want to filter on | (optional) defaults to undefined|


### Return type

**TagList**

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

# **tagsIdGet**
> TagReturn tagsIdGet()


### Example

```typescript
import {
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

let id: string; // (default to undefined)

const { status, data } = await apiInstance.tagsIdGet(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**TagReturn**

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

# **tagsPost**
> TagReturn tagsPost()


### Example

```typescript
import {
    ComposeApi,
    Configuration,
    Tag
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

let tag: Tag; // (optional)

const { status, data } = await apiInstance.tagsPost(
    tag
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tag** | **Tag**|  | |


### Return type

**TagReturn**

### Authorization

[JSON-Web-Token](../README.md#JSON-Web-Token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

