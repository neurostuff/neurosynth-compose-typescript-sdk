# DefaultApi

All URIs are relative to *https://compose.neurosynth.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**metaAnalysesIdDelete**](#metaanalysesiddelete) | **DELETE** /meta-analyses/{id} | |
|[**neurostoreAnnotationsIdGet**](#neurostoreannotationsidget) | **GET** /neurostore-annotations/{id} | Get a Neurostore annotation reference by Neurostore ID|
|[**neurostoreStudiesGet**](#neurostorestudiesget) | **GET** /neurostore-studies | Your GET endpoint|
|[**neurostoreStudiesIdGet**](#neurostorestudiesidget) | **GET** /neurostore-studies/{id} | Your GET endpoint|
|[**neurostoreStudiesIdPut**](#neurostorestudiesidput) | **PUT** /neurostore-studies/{id} | |
|[**neurostoreStudiesPost**](#neurostorestudiespost) | **POST** /neurostore-studies | |
|[**neurostoreStudysetsGet**](#neurostorestudysetsget) | **GET** /neurostore-studysets | List Neurostore studyset references|
|[**neurostoreStudysetsIdGet**](#neurostorestudysetsidget) | **GET** /neurostore-studysets/{id} | Get a Neurostore studyset reference by Neurostore ID|

# **metaAnalysesIdDelete**
> metaAnalysesIdDelete()


### Example

```typescript
import {
    DefaultApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DefaultApi(configuration);

let id: string; // (default to undefined)

const { status, data } = await apiInstance.metaAnalysesIdDelete(
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

# **neurostoreAnnotationsIdGet**
> AnnotationReferenceReturn neurostoreAnnotationsIdGet()

Resolve a Neurostore annotation reference using the same ID exposed by the Neurostore API.

### Example

```typescript
import {
    DefaultApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DefaultApi(configuration);

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
    DefaultApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DefaultApi(configuration);

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
    DefaultApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DefaultApi(configuration);

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

# **neurostoreStudiesIdPut**
> NeurostoreStudyReturn neurostoreStudiesIdPut()


### Example

```typescript
import {
    DefaultApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DefaultApi(configuration);

let id: string; // (default to undefined)

const { status, data } = await apiInstance.neurostoreStudiesIdPut(
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

[JSON-Web-Token](../README.md#JSON-Web-Token)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **neurostoreStudiesPost**
> NeurostoreStudyReturn neurostoreStudiesPost()


### Example

```typescript
import {
    DefaultApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DefaultApi(configuration);

const { status, data } = await apiInstance.neurostoreStudiesPost();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**NeurostoreStudyReturn**

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

# **neurostoreStudysetsGet**
> StudysetReferenceList neurostoreStudysetsGet()

List reference rows keyed by the actual Neurostore studyset ID.

### Example

```typescript
import {
    DefaultApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DefaultApi(configuration);

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

Resolve a Neurostore studyset reference using the same ID exposed by the Neurostore API. By default, this returns each linked snapshot with its compose snapshot ID and md5.

### Example

```typescript
import {
    DefaultApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DefaultApi(configuration);

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

