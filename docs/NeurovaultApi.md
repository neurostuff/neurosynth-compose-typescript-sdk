# NeurovaultApi

All URIs are relative to *https://compose.neurosynth.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**neurovaultCollectionsGet**](#neurovaultcollectionsget) | **GET** /neurovault-collections | Get neurovault collections|
|[**neurovaultCollectionsIdGet**](#neurovaultcollectionsidget) | **GET** /neurovault-collections/{id} | Your GET endpoint|
|[**neurovaultCollectionsIdPut**](#neurovaultcollectionsidput) | **PUT** /neurovault-collections/{id} | |
|[**neurovaultCollectionsPost**](#neurovaultcollectionspost) | **POST** /neurovault-collections | Create neurovault collection|
|[**neurovaultFilesGet**](#neurovaultfilesget) | **GET** /neurovault-files | Your GET endpoint|
|[**neurovaultFilesIdGet**](#neurovaultfilesidget) | **GET** /neurovault-files/{id} | Your GET endpoint|
|[**neurovaultFilesIdPut**](#neurovaultfilesidput) | **PUT** /neurovault-files/{id} | |
|[**neurovaultFilesPost**](#neurovaultfilespost) | **POST** /neurovault-files | |

# **neurovaultCollectionsGet**
> neurovaultCollectionsGet()


### Example

```typescript
import {
    NeurovaultApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new NeurovaultApi(configuration);

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
    NeurovaultApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new NeurovaultApi(configuration);

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
    NeurovaultApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new NeurovaultApi(configuration);

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
    NeurovaultApi,
    Configuration,
    NeurovaultCollection
} from './api';

const configuration = new Configuration();
const apiInstance = new NeurovaultApi(configuration);

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
    NeurovaultApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new NeurovaultApi(configuration);

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
    NeurovaultApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new NeurovaultApi(configuration);

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
    NeurovaultApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new NeurovaultApi(configuration);

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
    NeurovaultApi,
    Configuration,
    NeurovaultFile
} from './api';

const configuration = new Configuration();
const apiInstance = new NeurovaultApi(configuration);

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

