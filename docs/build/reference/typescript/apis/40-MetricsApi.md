# Metrics API

All URIs are relative to *http://localhost:1000*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getMetricsFormats**](MetricsApi#getmetricsformats) | **GET** /metrics/formats | /metrics/formats [GET]
[**metricsFormatsOrdered**](MetricsApi#metricsformatsordered) | **GET** /metrics/formats/ordered | /metrics/formats/ordered [GET]


## **getMetricsFormats**
> FormatsMetrics getMetricsFormats()

This is going to get a snapshot of our FormatsMetrics

### Example

```typescript
import * as Pieces from @pieces.app/pieces-os-client

// TODO: Write logic for os here
const configuration = Pieces.Configuration();
const apiInstance = new Pieces.MetricsApi(configuration);

apiInstance.getMetricsFormats().then((data: FormatsMetrics) => {
    console.log('API called successfully. Returned data: ' + data);
}).catch((error: unknown) => console.error(error));
```

### Parameters
This endpoint does not need any parameter.


### Return type

**FormatsMetrics**

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |



## **metricsFormatsOrdered**
> OrderedMetrics metricsFormatsOrdered()

This will return a list of code formats in desc order from most to least formats uploaded.

### Example

```typescript
import * as Pieces from @pieces.app/pieces-os-client

// TODO: Write logic for os here
const configuration = Pieces.Configuration();
const apiInstance = new Pieces.MetricsApi(configuration);

apiInstance.metricsFormatsOrdered().then((data: OrderedMetrics) => {
    console.log('API called successfully. Returned data: ' + data);
}).catch((error: unknown) => console.error(error));
```

### Parameters
This endpoint does not need any parameter.


### Return type

**OrderedMetrics**

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |



