# Linkify API

All URIs are relative to *http://localhost:1000*

Method | HTTP request | Description
------------- | ------------- | -------------
[**linkify**](LinkifyApi#linkify) | **POST** /linkify | /linkify [POST]
[**linkifyMultiple**](LinkifyApi#linkifyMultiple) | **POST** /linkify/multiple | /linkify/multiple [POST]
[**linkifyShareRevoke**](LinkifyApi#linkifyShareRevoke) | **POST** /linkify/\{share\}/revoke | [POST} /linkify/\{share\}/revoke


<a id="linkify"></a>
## **linkify**
> Shares linkify(linkify)

/linkify [POST]



### Example
```kotlin
// Import classes:
//import org.openapitools.client.infrastructure.*
//import org.openapitools.client.models.*

val apiInstance = LinkifyApi()
val linkify : Linkify =  // Linkify | 
try {
    val result : Shares = apiInstance.linkify(linkify)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling LinkifyApi#linkify")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling LinkifyApi#linkify")
    e.printStackTrace()
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **linkify** | [**Linkify**](Linkify)|  | [optional]

### Return type

[**Shares**](Shares)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="linkifyMultiple"></a>
## **linkifyMultiple**
> Shares linkifyMultiple(linkifyMultiple)

/linkify/multiple [POST]

- assumption that you have already backed up the asset&#39;s that you are sending to this endpoint.(b/c the assets are ids.)

### Example
```kotlin
// Import classes:
//import org.openapitools.client.infrastructure.*
//import org.openapitools.client.models.*

val apiInstance = LinkifyApi()
val linkifyMultiple : LinkifyMultiple =  // LinkifyMultiple | 
try {
    val result : Shares = apiInstance.linkifyMultiple(linkifyMultiple)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling LinkifyApi#linkifyMultiple")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling LinkifyApi#linkifyMultiple")
    e.printStackTrace()
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **linkifyMultiple** | [**LinkifyMultiple**](LinkifyMultiple)|  | [optional]

### Return type

[**Shares**](Shares)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="linkifyShareRevoke"></a>
## **linkifyShareRevoke**
> kotlin.String linkifyShareRevoke(share)

[POST} /linkify/\{share\}/revoke

This will revoke a link.

### Example
```kotlin
// Import classes:
//import org.openapitools.client.infrastructure.*
//import org.openapitools.client.models.*

val apiInstance = LinkifyApi()
val share : kotlin.String = share_example // kotlin.String | 
try {
    val result : kotlin.String = apiInstance.linkifyShareRevoke(share)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling LinkifyApi#linkifyShareRevoke")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling LinkifyApi#linkifyShareRevoke")
    e.printStackTrace()
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **share** | **kotlin.String**|  |

### Return type

**kotlin.String**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json
