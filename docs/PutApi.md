# PutApi

All URIs are relative to *https://compose.neurosynth.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**annotationsIdPut**](#annotationsidput) | **PUT** /annotations/{id} | Update an Annotation|
|[**metaAnalysesIdPut**](#metaanalysesidput) | **PUT** /meta-analyses/{id} | Update a meta-analysis|
|[**metaAnalysisResultsIdPut**](#metaanalysisresultsidput) | **PUT** /meta-analysis-results/{id} | |
|[**projectsIdPut**](#projectsidput) | **PUT** /projects/{id} | |
|[**specificationsIdPut**](#specificationsidput) | **PUT** /specifications/{id} | Update Meta-Analysis specification|
|[**studysetsIdPut**](#studysetsidput) | **PUT** /studysets/{id} | Update a Studyset|

# **annotationsIdPut**
> AnnotationReturn annotationsIdPut()

update an existing annotation

### Example

```typescript
import {
    PutApi,
    Configuration,
    AnnotationUpdate
} from './api';

const configuration = new Configuration();
const apiInstance = new PutApi(configuration);

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

# **metaAnalysesIdPut**
> MetaAnalysisReturn metaAnalysesIdPut()

update an existing meta-analysis (that has not yet been run)

### Example

```typescript
import {
    PutApi,
    Configuration,
    MetaAnalysis
} from './api';

const configuration = new Configuration();
const apiInstance = new PutApi(configuration);

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

# **metaAnalysisResultsIdPut**
> ResultReturn metaAnalysisResultsIdPut()


### Example

```typescript
import {
    PutApi,
    Configuration,
    Result
} from './api';

const configuration = new Configuration();
const apiInstance = new PutApi(configuration);

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

# **projectsIdPut**
> ProjectReturn projectsIdPut()


### Example

```typescript
import {
    PutApi,
    Configuration,
    Project
} from './api';

const configuration = new Configuration();
const apiInstance = new PutApi(configuration);

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

# **specificationsIdPut**
> SpecificationReturn specificationsIdPut()

update an existing meta analysis specification

### Example

```typescript
import {
    PutApi,
    Configuration,
    Specification
} from './api';

const configuration = new Configuration();
const apiInstance = new PutApi(configuration);

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

# **studysetsIdPut**
> StudysetReturn studysetsIdPut()

update an existing serialized/referenced studyset

### Example

```typescript
import {
    PutApi,
    Configuration,
    Studyset
} from './api';

const configuration = new Configuration();
const apiInstance = new PutApi(configuration);

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

