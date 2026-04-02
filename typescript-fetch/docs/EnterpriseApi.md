# EnterpriseApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**enterpriseControllerAuth**](EnterpriseApi.md#enterprisecontrollerauth) | **POST** /enterprise/auth | Authenticate and retrieve OAuth2 token |
| [**enterpriseControllerImportClients**](EnterpriseApi.md#enterprisecontrollerimportclients) | **POST** /enterprise/import-clients | Import enterprise clients |



## enterpriseControllerAuth

> any enterpriseControllerAuth(authDTO)

Authenticate and retrieve OAuth2 token

Exchanges your enterprise client credentials for an OAuth2 access token. This token is required for accessing protected enterprise endpoints including import-clients and document operations. 

### Example

```ts
import {
  Configuration,
  EnterpriseApi,
} from '';
import type { EnterpriseControllerAuthRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const api = new EnterpriseApi();

  const body = {
    // AuthDTO
    authDTO: {"clientId":"abc123xyz789","clientSecret":"secret_key_12345"},
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

**any**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully authenticated. Access token returned with doc/upload scope. |  -  |
| **201** |  |  -  |
| **401** | Invalid client credentials provided. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## enterpriseControllerImportClients

> any enterpriseControllerImportClients(importClientsDTO)

Import enterprise clients

Imports a list of clients into your organization. Requires a valid OAuth2 access token obtained from the /auth endpoint. Each client will be added to your organization with the provided email and unique external client ID.  The clientId will serve as an external identifier to track which enterprise client each consumer belongs to. Critically, this clientId mapping determines document upload behavior: documents uploaded by imported clients will be stored unencrypted (enterprise-managed storage). Clients will be created in Cognito if they do not already exist, and their association with your organization and the provided clientId will be stored in the system.  Import Format: A customer-generated CSV file will be used to onboard multiple users in bulk. The CSV file will have the following format:  clientEmail,clientId  When using the Brands App, the user\&#39;s email will be used as the clientEmail and the initial password will be an OTP sent to the user\&#39;s email. The clientId will be any unique identifier from your enterprise system that you want to associate with this client. This will allow you to maintain a mapping between your enterprise system and the consumers created in this platform, and will enable unencrypted document storage for these clients.  

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
    importClientsDTO: {"clients":[{"clientEmail":"client@example.com","clientId":"client_001"}]},
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

**any**

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Clients successfully imported. Returns an empty response body. |  -  |
| **400** | Invalid request body. Ensure clients array has at least 1 item and all fields are valid. |  -  |
| **401** | Unauthorized. Invalid or missing OAuth2 token. |  -  |
| **403** | Forbidden. Your organization does not have enterprise access. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

