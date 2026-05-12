# ComposeApi

All URIs are relative to *https://compose.neurosynth.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**metaAnalysesGet**](#metaanalysesget) | **GET** /meta-analyses | GET a list of meta-analyses|
|[**metaAnalysesIdGet**](#metaanalysesidget) | **GET** /meta-analyses/{id} | GET meta-analysis information|
|[**metaAnalysesIdPut**](#metaanalysesidput) | **PUT** /meta-analyses/{id} | Update a meta-analysis|
|[**metaAnalysesPost**](#metaanalysespost) | **POST** /meta-analyses | Create a new meta-analysis|
|[**metaAnalysisJobsGet**](#metaanalysisjobsget) | **GET** /meta-analysis-jobs | List meta-analysis jobs for the current user|
|[**metaAnalysisJobsJobIdGet**](#metaanalysisjobsjobidget) | **GET** /meta-analysis-jobs/{job_id} | Get status and logs for a meta-analysis job|
|[**metaAnalysisJobsPost**](#metaanalysisjobspost) | **POST** /meta-analysis-jobs | Submit a meta-analysis job|
|[**metaAnalysisResultsGet**](#metaanalysisresultsget) | **GET** /meta-analysis-results | List meta-analysis results|
|[**metaAnalysisResultsIdGet**](#metaanalysisresultsidget) | **GET** /meta-analysis-results/{id} | Get a meta-analysis result by ID|
|[**metaAnalysisResultsIdPut**](#metaanalysisresultsidput) | **PUT** /meta-analysis-results/{id} | Update a meta-analysis result with files or snapshots|
|[**metaAnalysisResultsPost**](#metaanalysisresultspost) | **POST** /meta-analysis-results | Create a new meta-analysis result|
|[**neurostoreAnnotationsIdGet**](#neurostoreannotationsidget) | **GET** /neurostore-annotations/{id} | Get a Neurostore annotation reference by Neurostore ID|
|[**neurostoreStudiesGet**](#neurostorestudiesget) | **GET** /neurostore-studies | Your GET endpoint|
|[**neurostoreStudiesIdGet**](#neurostorestudiesidget) | **GET** /neurostore-studies/{id} | Your GET endpoint|
|[**neurostoreStudysetsGet**](#neurostorestudysetsget) | **GET** /neurostore-studysets | List Neurostore studyset references|
|[**neurostoreStudysetsIdGet**](#neurostorestudysetsidget) | **GET** /neurostore-studysets/{id} | Get a Neurostore studyset reference by Neurostore ID|
|[**neurovaultCollectionsGet**](#neurovaultcollectionsget) | **GET** /neurovault-collections | Get neurovault collections|
|[**neurovaultCollectionsIdGet**](#neurovaultcollectionsidget) | **GET** /neurovault-collections/{id} | Your GET endpoint|
|[**neurovaultCollectionsIdPut**](#neurovaultcollectionsidput) | **PUT** /neurovault-collections/{id} | |
|[**neurovaultCollectionsPost**](#neurovaultcollectionspost) | **POST** /neurovault-collections | Create neurovault collection|
|[**neurovaultFilesGet**](#neurovaultfilesget) | **GET** /neurovault-files | Your GET endpoint|
|[**neurovaultFilesIdGet**](#neurovaultfilesidget) | **GET** /neurovault-files/{id} | Your GET endpoint|
|[**neurovaultFilesIdPut**](#neurovaultfilesidput) | **PUT** /neurovault-files/{id} | |
|[**neurovaultFilesPost**](#neurovaultfilespost) | **POST** /neurovault-files | |
|[**projectsGet**](#projectsget) | **GET** /projects | Your GET endpoint|
|[**projectsIdDelete**](#projectsiddelete) | **DELETE** /projects/{id} | |
|[**projectsIdGet**](#projectsidget) | **GET** /projects/{id} | Your GET endpoint|
|[**projectsIdPut**](#projectsidput) | **PUT** /projects/{id} | |
|[**projectsPost**](#projectspost) | **POST** /projects | |
|[**snapshotAnnotationsGet**](#snapshotannotationsget) | **GET** /snapshot-annotations | GET a list of annotations|
|[**snapshotAnnotationsIdGet**](#snapshotannotationsidget) | **GET** /snapshot-annotations/{id} | GET information about an annotation|
|[**snapshotAnnotationsIdPut**](#snapshotannotationsidput) | **PUT** /snapshot-annotations/{id} | Update an Annotation|
|[**snapshotAnnotationsPost**](#snapshotannotationspost) | **POST** /snapshot-annotations | Create a new Annotation|
|[**snapshotStudysetsGet**](#snapshotstudysetsget) | **GET** /snapshot-studysets | Get a list of Studysets|
|[**snapshotStudysetsIdGet**](#snapshotstudysetsidget) | **GET** /snapshot-studysets/{id} | Get information about a Studyset|
|[**snapshotStudysetsIdPut**](#snapshotstudysetsidput) | **PUT** /snapshot-studysets/{id} | Update a Studyset|
|[**snapshotStudysetsPost**](#snapshotstudysetspost) | **POST** /snapshot-studysets | Create a new Studyset|
|[**specificationsGet**](#specificationsget) | **GET** /specifications | Get a list of Specifications|
|[**specificationsIdGet**](#specificationsidget) | **GET** /specifications/{id} | Get information about a Specification|
|[**specificationsIdPut**](#specificationsidput) | **PUT** /specifications/{id} | Update Meta-Analysis specification|
|[**specificationsPost**](#specificationspost) | **POST** /specifications | Create a Specification|
|[**tagsGet**](#tagsget) | **GET** /tags | Get a list of Tags|
|[**tagsIdGet**](#tagsidget) | **GET** /tags/{id} | Get information about a Tag|
|[**tagsPost**](#tagspost) | **POST** /tags | Create a new Tag|
|[**usersGet**](#usersget) | **GET** /users | GET list of Users|
|[**usersIdGet**](#usersidget) | **GET** /users/{id} | Get User Info by User ID|
|[**usersIdPut**](#usersidput) | **PUT** /users/{id} | Update User Information|
|[**usersPost**](#userspost) | **POST** /users | Create A New User|

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

# **metaAnalysisJobsGet**
> MetaAnalysisJobList metaAnalysisJobsGet()

Return cached job submissions associated with the authenticated user.

### Example

```typescript
import {
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

const { status, data } = await apiInstance.metaAnalysisJobsGet();
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

# **metaAnalysisJobsJobIdGet**
> MetaAnalysisJobResponse metaAnalysisJobsJobIdGet()

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

const { status, data } = await apiInstance.metaAnalysisJobsJobIdGet(
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

# **metaAnalysisJobsPost**
> MetaAnalysisJobResponse metaAnalysisJobsPost(metaAnalysisJobRequest)

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

const { status, data } = await apiInstance.metaAnalysisJobsPost(
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

# **neurostoreAnnotationsIdGet**
> AnnotationReferenceReturn neurostoreAnnotationsIdGet()

Resolve a Neurostore annotation reference using the same ID exposed by the Neurostore API, including each linked snapshot\'s compose ID and md5.

### Example

```typescript
import {
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

let id: string; // (default to undefined)

const { status, data } = await apiInstance.neurostoreAnnotationsIdGet(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**AnnotationReferenceReturn**

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

# **neurostoreStudiesGet**
> NeurostoreStudyList neurostoreStudiesGet()


### Example

```typescript
import {
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

const { status, data } = await apiInstance.neurostoreStudiesGet();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**NeurostoreStudyList**

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

# **neurostoreStudiesIdGet**
> NeurostoreStudyReturn neurostoreStudiesIdGet()


### Example

```typescript
import {
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

let id: string; // (default to undefined)

const { status, data } = await apiInstance.neurostoreStudiesIdGet(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**NeurostoreStudyReturn**

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

# **neurostoreStudysetsGet**
> StudysetReferenceList neurostoreStudysetsGet()

List reference rows keyed by the actual Neurostore studyset ID, including compact snapshot summaries.

### Example

```typescript
import {
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

let nested: boolean; //show nested component instead of id (optional) (default to undefined)

const { status, data } = await apiInstance.neurostoreStudysetsGet(
    nested
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **nested** | [**boolean**] | show nested component instead of id | (optional) defaults to undefined|


### Return type

**StudysetReferenceList**

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

# **neurostoreStudysetsIdGet**
> StudysetReferenceReturn neurostoreStudysetsIdGet()

Resolve a Neurostore studyset reference using the same ID exposed by the Neurostore API, including each linked snapshot\'s compose ID and md5.

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

const { status, data } = await apiInstance.neurostoreStudysetsIdGet(
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

**StudysetReferenceReturn**

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

# **neurovaultCollectionsGet**
> neurovaultCollectionsGet()


### Example

```typescript
import {
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

const { status, data } = await apiInstance.neurovaultCollectionsGet();
```

### Parameters
This endpoint does not have any parameters.


### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **neurovaultCollectionsIdGet**
> NeurovaultCollectionReturn neurovaultCollectionsIdGet()


### Example

```typescript
import {
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

let id: string; // (default to undefined)

const { status, data } = await apiInstance.neurovaultCollectionsIdGet(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**NeurovaultCollectionReturn**

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

# **neurovaultCollectionsIdPut**
> NeurovaultCollectionReturn neurovaultCollectionsIdPut()


### Example

```typescript
import {
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

let id: string; // (default to undefined)

const { status, data } = await apiInstance.neurovaultCollectionsIdPut(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**NeurovaultCollectionReturn**

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

# **neurovaultCollectionsPost**
> neurovaultCollectionsPost()



### Example

```typescript
import {
    ComposeApi,
    Configuration,
    NeurovaultCollection
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

let neurovaultCollection: NeurovaultCollection; // (optional)

const { status, data } = await apiInstance.neurovaultCollectionsPost(
    neurovaultCollection
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **neurovaultCollection** | **NeurovaultCollection**|  | |


### Return type

void (empty response body)

### Authorization

[JSON-Web-Token](../README.md#JSON-Web-Token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **neurovaultFilesGet**
> NeurovaultFileList neurovaultFilesGet()


### Example

```typescript
import {
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

const { status, data } = await apiInstance.neurovaultFilesGet();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**NeurovaultFileList**

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

# **neurovaultFilesIdGet**
> NeurovaultFileReturn neurovaultFilesIdGet()


### Example

```typescript
import {
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

let id: string; // (default to undefined)

const { status, data } = await apiInstance.neurovaultFilesIdGet(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**NeurovaultFileReturn**

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

# **neurovaultFilesIdPut**
> NeurovaultFileReturn neurovaultFilesIdPut()


### Example

```typescript
import {
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

let id: string; // (default to undefined)
let collectionId: string; // (optional) (default to undefined)
let exception: string; // (optional) (default to undefined)
let traceback: string; // (optional) (default to undefined)
let status: string; // (optional) (default to undefined)
let imageId: string; // (optional) (default to undefined)
let name: string; // (optional) (default to undefined)
let url: string; // (optional) (default to undefined)

const { status, data } = await apiInstance.neurovaultFilesIdPut(
    id,
    collectionId,
    exception,
    traceback,
    status,
    imageId,
    name,
    url
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] |  | defaults to undefined|
| **collectionId** | [**string**] |  | (optional) defaults to undefined|
| **exception** | [**string**] |  | (optional) defaults to undefined|
| **traceback** | [**string**] |  | (optional) defaults to undefined|
| **status** | [**string**] |  | (optional) defaults to undefined|
| **imageId** | [**string**] |  | (optional) defaults to undefined|
| **name** | [**string**] |  | (optional) defaults to undefined|
| **url** | [**string**] |  | (optional) defaults to undefined|


### Return type

**NeurovaultFileReturn**

### Authorization

[JSON-Web-Token](../README.md#JSON-Web-Token)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **neurovaultFilesPost**
> NeurovaultFileReturn neurovaultFilesPost()


### Example

```typescript
import {
    ComposeApi,
    Configuration,
    NeurovaultFile
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

let neurovaultFile: NeurovaultFile; // (optional)

const { status, data } = await apiInstance.neurovaultFilesPost(
    neurovaultFile
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **neurovaultFile** | **NeurovaultFile**|  | |


### Return type

**NeurovaultFileReturn**

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
let includeProvenance: boolean; //include the project provenance payload in project responses (optional) (default to true)

const { status, data } = await apiInstance.projectsGet(
    page,
    pageSize,
    name,
    search,
    description,
    sort,
    desc,
    userId,
    includeProvenance
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
| **includeProvenance** | [**boolean**] | include the project provenance payload in project responses | (optional) defaults to true|


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
let includeProvenance: boolean; //include the project provenance payload in project responses (optional) (default to true)

const { status, data } = await apiInstance.projectsIdGet(
    id,
    info,
    includeProvenance
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] |  | defaults to undefined|
| **info** | [**boolean**] | display additional information about a nested relationship without displaying fully nested object | (optional) defaults to undefined|
| **includeProvenance** | [**boolean**] | include the project provenance payload in project responses | (optional) defaults to true|


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
let syncMetaAnalysesPublic: boolean; //when updating a project\'s public flag, also set each child meta-analysis to the same public value (optional) (default to undefined)
let project: Project; // (optional)

const { status, data } = await apiInstance.projectsIdPut(
    id,
    syncMetaAnalysesPublic,
    project
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **project** | **Project**|  | |
| **id** | [**string**] |  | defaults to undefined|
| **syncMetaAnalysesPublic** | [**boolean**] | when updating a project\&#39;s public flag, also set each child meta-analysis to the same public value | (optional) defaults to undefined|


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

# **snapshotAnnotationsGet**
> AnnotationList snapshotAnnotationsGet()

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

const { status, data } = await apiInstance.snapshotAnnotationsGet(
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

# **snapshotAnnotationsIdGet**
> AnnotationReturn snapshotAnnotationsIdGet()

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

const { status, data } = await apiInstance.snapshotAnnotationsIdGet(
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

# **snapshotAnnotationsIdPut**
> AnnotationReturn snapshotAnnotationsIdPut()

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

const { status, data } = await apiInstance.snapshotAnnotationsIdPut(
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

# **snapshotAnnotationsPost**
> AnnotationReturn snapshotAnnotationsPost()

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

const { status, data } = await apiInstance.snapshotAnnotationsPost(
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

# **snapshotStudysetsGet**
> StudysetList snapshotStudysetsGet()

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
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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
    ComposeApi,
    Configuration,
    Studyset
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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
    ComposeApi,
    Configuration,
    StudysetPostBody
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

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

# **usersGet**
> UserList usersGet()

List all users

### Example

```typescript
import {
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

const { status, data } = await apiInstance.usersGet();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**UserList**

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

# **usersIdGet**
> UserReturn usersIdGet()

Retrieve the information of the user with the matching user ID.

### Example

```typescript
import {
    ComposeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

let id: string; // (default to undefined)

const { status, data } = await apiInstance.usersIdGet(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**UserReturn**

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

# **usersIdPut**
> UserReturn usersIdPut()

update information about a user

### Example

```typescript
import {
    ComposeApi,
    Configuration,
    User
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

let id: string; // (default to undefined)
let user: User; // (optional)

const { status, data } = await apiInstance.usersIdPut(
    id,
    user
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **user** | **User**|  | |
| **id** | [**string**] |  | defaults to undefined|


### Return type

**UserReturn**

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

# **usersPost**
> UserReturn usersPost()

create a single user

### Example

```typescript
import {
    ComposeApi,
    Configuration,
    User
} from './api';

const configuration = new Configuration();
const apiInstance = new ComposeApi(configuration);

let user: User; // (optional)

const { status, data } = await apiInstance.usersPost(
    user
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **user** | **User**|  | |


### Return type

**UserReturn**

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

