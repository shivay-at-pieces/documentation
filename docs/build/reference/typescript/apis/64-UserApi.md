# User API

All URIs are relative to *http://localhost:1000*

Method | HTTP request | Description
------------- | ------------- | -------------
[**clearUser**](UserApi#clearuser) | **POST** /user/clear | /user/clear
[**refreshUser**](UserApi#refreshuser) | **GET** /user/refresh | /user/refresh [GET]
[**selectUser**](UserApi#selectuser) | **POST** /user/select | /user/select [POST]
[**streamUser**](UserApi#streamuser) | **GET** /user/stream | /user/stream [GET]
[**updateUser**](UserApi#updateuser) | **POST** /user/update | /user/update [POST]
[**userProviders**](UserApi#userproviders) | **GET** /user/providers | Your GET endpoint
[**userSnapshot**](UserApi#usersnapshot) | **GET** /user | /user [GET]
[**userUpdateVanity**](UserApi#userupdatevanity) | **POST** /user/update/vanity | /user/update/vanity [POST]


## **clearUser**
> clearUser()

An endpoint to clear the current user. 

### Example

```typescript
import * as Pieces from @pieces.app/pieces-os-client

// TODO: Write logic for os here
const configuration = Pieces.Configuration();
const apiInstance = new Pieces.UserApi(configuration);

apiInstance.clearUser().then((data: void (empty response body)) => {
    console.log('API called successfully. Returned data: ' + data);
}).catch((error: unknown) => console.error(error));
```

### Parameters
This endpoint does not need any parameter.


### Return type

void (empty response body)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | No Content |  -  |



## **refreshUser**
> UserProfile refreshUser()

This will refresh a user.

### Example

```typescript
import * as Pieces from @pieces.app/pieces-os-client

// TODO: Write logic for os here
const configuration = Pieces.Configuration();
const apiInstance = new Pieces.UserApi(configuration);

apiInstance.refreshUser().then((data: UserProfile) => {
    console.log('API called successfully. Returned data: ' + data);
}).catch((error: unknown) => console.error(error));
```

### Parameters
This endpoint does not need any parameter.


### Return type

**UserProfile**

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**500** | Internal Server Error |  -  |



## **selectUser**
> UserProfile selectUser()

This will select the current user.

### Example

```typescript
import * as Pieces from @pieces.app/pieces-os-client

// TODO: Write logic for os here
const configuration = Pieces.Configuration();
const apiInstance = new Pieces.UserApi(configuration);

const body: Pieces.SelectUserRequest = {
    // Auth0User |  (optional)
    auth0User: ,
};

apiInstance.selectUser(body).then((data: UserProfile) => {
    console.log('API called successfully. Returned data: ' + data);
}).catch((error: unknown) => console.error(error));
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **auth0User** | **Auth0User**|  |


### Return type

**UserProfile**

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |



## **streamUser**
> UserProfile streamUser()

This will stream in the current user, not quiet sure yet how we want to do this.

### Example

```typescript
import * as Pieces from @pieces.app/pieces-os-client

// TODO: Write logic for os here
const configuration = Pieces.Configuration();
const apiInstance = new Pieces.UserApi(configuration);

apiInstance.streamUser().then((data: UserProfile) => {
    console.log('API called successfully. Returned data: ' + data);
}).catch((error: unknown) => console.error(error));
```

### Parameters
This endpoint does not need any parameter.


### Return type

**UserProfile**

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |



## **updateUser**
> UserProfile updateUser()

This will update a specific user in the database.

### Example

```typescript
import * as Pieces from @pieces.app/pieces-os-client

// TODO: Write logic for os here
const configuration = Pieces.Configuration();
const apiInstance = new Pieces.UserApi(configuration);

const body: Pieces.UpdateUserRequest = {
    // UserProfile |  (optional)
    userProfile: ,
};

apiInstance.updateUser(body).then((data: UserProfile) => {
    console.log('API called successfully. Returned data: ' + data);
}).catch((error: unknown) => console.error(error));
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userProfile** | **UserProfile**|  |


### Return type

**UserProfile**

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |



## **userProviders**
> ReturnedUserProfile userProviders()

This will retrieve all the users Providers that are connected to this account.  If called locally. we will 501 - because it is not implemented locally yet.  If called in the cloud, we will refresh && get your access tokens to access these providers.

### Example

```typescript
import * as Pieces from @pieces.app/pieces-os-client

// TODO: Write logic for os here
const configuration = Pieces.Configuration();
const apiInstance = new Pieces.UserApi(configuration);

apiInstance.userProviders().then((data: ReturnedUserProfile) => {
    console.log('API called successfully. Returned data: ' + data);
}).catch((error: unknown) => console.error(error));
```

### Parameters
This endpoint does not need any parameter.


### Return type

**ReturnedUserProfile**

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**500** | Internal Server Error |  -  |
**501** | Not Implemented |  -  |



## **userSnapshot**
> ReturnedUserProfile userSnapshot()

This will return a snapshot of the current user. This will return our ReturnUserProfile and the user on that object is just a UserProfile and can potentially be null.

### Example

```typescript
import * as Pieces from @pieces.app/pieces-os-client

// TODO: Write logic for os here
const configuration = Pieces.Configuration();
const apiInstance = new Pieces.UserApi(configuration);

apiInstance.userSnapshot().then((data: ReturnedUserProfile) => {
    console.log('API called successfully. Returned data: ' + data);
}).catch((error: unknown) => console.error(error));
```

### Parameters
This endpoint does not need any parameter.


### Return type

**ReturnedUserProfile**

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |



## **userUpdateVanity**
> UserProfile userUpdateVanity()

This is a local route to update your vanityname. ie mark.pieces.cloud, where \"mark\" is the vanityname.

### Example

```typescript
import * as Pieces from @pieces.app/pieces-os-client

// TODO: Write logic for os here
const configuration = Pieces.Configuration();
const apiInstance = new Pieces.UserApi(configuration);

const body: Pieces.UserUpdateVanityRequest = {
    // UserProfile | This will take an update userProfile, with the updated vanity name! (optional)
    userProfile: ,
};

apiInstance.userUpdateVanity(body).then((data: UserProfile) => {
    console.log('API called successfully. Returned data: ' + data);
}).catch((error: unknown) => console.error(error));
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userProfile** | **UserProfile**| This will take an update userProfile, with the updated vanity name! |


### Return type

**UserProfile**

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**404** | The original dns record was not found, please wait for cloud connectivity to fully connect. |  -  |
**409** | Conflict, This means that we were unable to update the username because it was already taken. |  -  |
**500** | Unable to create a username. Internal Server Error. |  -  |
**511** | Network Authentication Required, Cannot Update the Vanityname of the user because the user is either not signed in or in not connected to the cloud. |  -  |



