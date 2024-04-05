# Model API

All URIs are relative to *http://localhost:1000*

Method | HTTP request | Description
------------- | ------------- | -------------
[**modelSpecificModelDownload**](ModelApi#modelspecificmodeldownload) | **POST** /model/\{model\}/download | /model/\{model\}/download [POST]
[**modelSpecificModelDownloadCancel**](ModelApi#modelspecificmodeldownloadcancel) | **POST** /model/\{model\}/download/cancel | /model/\{model\}/download/cancel [POST]
[**modelSpecificModelDownloadProgress**](ModelApi#modelspecificmodeldownloadprogress) | **GET** /model/\{model\}/download/progress | /model/\{model\}/download/progress [WS]
[**modelSpecificModelLoad**](ModelApi#modelspecificmodelload) | **POST** /model/\{model\}/load | /model/\{model\}/load [POST]
[**modelSpecificModelUnload**](ModelApi#modelspecificmodelunload) | **POST** /model/\{model\}/unload | /model/\{model\}/unload [POST]
[**modelUpdate**](ModelApi#modelupdate) | **POST** /model/update | /model/update [POST]
[**modelsSpecificModelSnapshot**](ModelApi#modelsspecificmodelsnapshot) | **GET** /model/\{model\} | /model/\{model\} [GET]


## **modelSpecificModelDownload**
> Model modelSpecificModelDownload()

This will download a specific model onto your local machine.

### Example

```typescript
import * as Pieces from @pieces.app/pieces-os-client

// TODO: Write logic for os here
const configuration = Pieces.Configuration();
const apiInstance = new Pieces.ModelApi(configuration);

const body: Pieces.ModelSpecificModelDownloadRequest = {
    // string | model id
    model: model_example,
};

apiInstance.modelSpecificModelDownload(body).then((data: Model) => {
    console.log('API called successfully. Returned data: ' + data);
}).catch((error: unknown) => console.error(error));
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model** | [**string**] | model id | defaults to undefined


### Return type

**Model**

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**500** | Internal Server Error |  -  |



## **modelSpecificModelDownloadCancel**
> Model modelSpecificModelDownloadCancel()

This will cancel a specific model download in progress.

### Example

```typescript
import * as Pieces from @pieces.app/pieces-os-client

// TODO: Write logic for os here
const configuration = Pieces.Configuration();
const apiInstance = new Pieces.ModelApi(configuration);

const body: Pieces.ModelSpecificModelDownloadCancelRequest = {
    // string | model id
    model: model_example,
};

apiInstance.modelSpecificModelDownloadCancel(body).then((data: Model) => {
    console.log('API called successfully. Returned data: ' + data);
}).catch((error: unknown) => console.error(error));
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model** | [**string**] | model id | defaults to undefined


### Return type

**Model**

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**500** | Internal Server Error |  -  |



## **modelSpecificModelDownloadProgress**
> ModelDownloadProgress modelSpecificModelDownloadProgress()

This is a Websocket Connection, to get the progress of the downloading of a specific model.

### Example

```typescript
import * as Pieces from @pieces.app/pieces-os-client

// TODO: Write logic for os here
const configuration = Pieces.Configuration();
const apiInstance = new Pieces.ModelApi(configuration);

const body: Pieces.ModelSpecificModelDownloadProgressRequest = {
    // string | model id
    model: model_example,
};

apiInstance.modelSpecificModelDownloadProgress(body).then((data: ModelDownloadProgress) => {
    console.log('API called successfully. Returned data: ' + data);
}).catch((error: unknown) => console.error(error));
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model** | [**string**] | model id | defaults to undefined


### Return type

**ModelDownloadProgress**

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**500** | Internal Server Error |  -  |



## **modelSpecificModelLoad**
> Model modelSpecificModelLoad()

This will load an already downloaded model into memory. This is different that downloading becuase downloading the entire model onto your machine, load will load the downloaded model into memory.

### Example

```typescript
import * as Pieces from @pieces.app/pieces-os-client

// TODO: Write logic for os here
const configuration = Pieces.Configuration();
const apiInstance = new Pieces.ModelApi(configuration);

const body: Pieces.ModelSpecificModelLoadRequest = {
    // string | model id
    model: model_example,
};

apiInstance.modelSpecificModelLoad(body).then((data: Model) => {
    console.log('API called successfully. Returned data: ' + data);
}).catch((error: unknown) => console.error(error));
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model** | [**string**] | model id | defaults to undefined


### Return type

**Model**

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**500** | Internal Server Error |  -  |



## **modelSpecificModelUnload**
> Model modelSpecificModelUnload()

This will unload an already loaded model from memory. This will free up the ram that this model is currently consuming.

### Example

```typescript
import * as Pieces from @pieces.app/pieces-os-client

// TODO: Write logic for os here
const configuration = Pieces.Configuration();
const apiInstance = new Pieces.ModelApi(configuration);

const body: Pieces.ModelSpecificModelUnloadRequest = {
    // string | model id
    model: model_example,
};

apiInstance.modelSpecificModelUnload(body).then((data: Model) => {
    console.log('API called successfully. Returned data: ' + data);
}).catch((error: unknown) => console.error(error));
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model** | [**string**] | model id | defaults to undefined


### Return type

**Model**

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**500** | Internal Server Error |  -  |



## **modelUpdate**
> Model modelUpdate()

This will update Machinelearning Model, this is only available for \"custom:true\" models.

### Example

```typescript
import * as Pieces from @pieces.app/pieces-os-client

// TODO: Write logic for os here
const configuration = Pieces.Configuration();
const apiInstance = new Pieces.ModelApi(configuration);

const body: Pieces.ModelUpdateRequest = {
    // Model (optional)
    model: ,
};

apiInstance.modelUpdate(body).then((data: Model) => {
    console.log('API called successfully. Returned data: ' + data);
}).catch((error: unknown) => console.error(error));
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model** | **Model**|  |


### Return type

**Model**

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**500** | Internal Server Error |  -  |



## **modelsSpecificModelSnapshot**
> Model modelsSpecificModelSnapshot()



### Example

```typescript
import * as Pieces from @pieces.app/pieces-os-client

// TODO: Write logic for os here
const configuration = Pieces.Configuration();
const apiInstance = new Pieces.ModelApi(configuration);

const body: Pieces.ModelsSpecificModelSnapshotRequest = {
    // string | model id
    model: model_example,
};

apiInstance.modelsSpecificModelSnapshot(body).then((data: Model) => {
    console.log('API called successfully. Returned data: ' + data);
}).catch((error: unknown) => console.error(error));
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model** | [**string**] | model id | defaults to undefined


### Return type

**Model**

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**410** | model was not found. |  -  |



