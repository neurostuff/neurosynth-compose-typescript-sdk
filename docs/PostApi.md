# PostApi

All URIs are relative to *https://compose.neurosynth.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**annotationsPost**](#annotationspost) | **POST** /annotations | Create a new Annotation|
|[**metaAnalysesPost**](#metaanalysespost) | **POST** /meta-analyses | Create a new meta-analysis|
|[**metaAnalysisResultsPost**](#metaanalysisresultspost) | **POST** /meta-analysis-results | |
|[**neurosynthComposeResourcesMetaAnalysisJobsMetaAnalysisJobsResourcePost**](#neurosynthcomposeresourcesmetaanalysisjobsmetaanalysisjobsresourcepost) | **POST** /meta-analysis-jobs | Submit a meta-analysis job|
|[**projectsPost**](#projectspost) | **POST** /projects | |
|[**specificationsPost**](#specificationspost) | **POST** /specifications | Create a Specification|
|[**studysetsPost**](#studysetspost) | **POST** /studysets | Create a new Studyset|

# **annotationsPost**
> AnnotationReturn annotationsPost()

create a new serialized/referenced annotation

### Example

```typescript
import {
    PostApi,
    Configuration,
    AnnotationPostBody
} from './api';

const configuration = new Configuration();
const apiInstance = new PostApi(configuration);

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

# **metaAnalysesPost**
> MetaAnalysisReturn metaAnalysesPost()

create a new specification, studyset, annotation bundle

### Example

```typescript
import {
    PostApi,
    Configuration,
    MetaAnalysisPostBody
} from './api';

const configuration = new Configuration();
const apiInstance = new PostApi(configuration);

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

# **metaAnalysisResultsPost**
> ResultReturn metaAnalysisResultsPost()


### Example

```typescript
import {
    PostApi,
    Configuration,
    ResultInit
} from './api';

const configuration = new Configuration();
const apiInstance = new PostApi(configuration);

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

# **neurosynthComposeResourcesMetaAnalysisJobsMetaAnalysisJobsResourcePost**
> MetaAnalysisJobResponse neurosynthComposeResourcesMetaAnalysisJobsMetaAnalysisJobsResourcePost(metaAnalysisJobRequest)

Submit a meta-analysis to the compose runner service.

### Example

```typescript
import {
    PostApi,
    Configuration,
    MetaAnalysisJobRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new PostApi(configuration);

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

# **projectsPost**
> ProjectReturn projectsPost()


### Example

```typescript
import {
    PostApi,
    Configuration,
    Project
} from './api';

const configuration = new Configuration();
const apiInstance = new PostApi(configuration);

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

# **specificationsPost**
> SpecificationReturn specificationsPost()

create a new meta-analysis specification

### Example

```typescript
import {
    PostApi,
    Configuration,
    SpecificationPostBody
} from './api';

const configuration = new Configuration();
const apiInstance = new PostApi(configuration);

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

# **studysetsPost**
> StudysetReturn studysetsPost()

create a new serialized/referenced studyset

### Example

```typescript
import {
    PostApi,
    Configuration,
    StudysetPostBody
} from './api';

const configuration = new Configuration();
const apiInstance = new PostApi(configuration);

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

