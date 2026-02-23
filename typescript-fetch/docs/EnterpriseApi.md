# EnterpriseApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**enterpriseControllerAuth**](EnterpriseApi.md#enterprisecontrollerauth) | **POST** /enterprise/auth |  |
| [**enterpriseControllerImportClients**](EnterpriseApi.md#enterprisecontrollerimportclients) | **POST** /enterprise/import-clients |  |



## enterpriseControllerAuth

> object enterpriseControllerAuth(authDTO)



### Example

```ts
import {
  Configuration,
  EnterpriseApi,
} from '';
import type { EnterpriseControllerAuthRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearer
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new EnterpriseApi(config);

  const body = {
    // AuthDTO
    authDTO: ...,
  } satisfies EnterpriseControllerAuthRequest;

  try {
    const data = await api.enterpriseControllerAuth(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **authDTO** | [AuthDTO](AuthDTO.md) |  | |

### Return type

**object**

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## enterpriseControllerImportClients

> object enterpriseControllerImportClients(importClientsDTO)



### Example

```ts
import {
  Configuration,
  EnterpriseApi,
} from '';
import type { EnterpriseControllerImportClientsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearer
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new EnterpriseApi(config);

  const body = {
    // ImportClientsDTO
    importClientsDTO: ...,
  } satisfies EnterpriseControllerImportClientsRequest;

  try {
    const data = await api.enterpriseControllerImportClients(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **importClientsDTO** | [ImportClientsDTO](ImportClientsDTO.md) |  | |

### Return type

**object**

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

