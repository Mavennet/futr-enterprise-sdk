# EnterpriseApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**enterpriseControllerAuth**](EnterpriseApi.md#enterprisecontrollerauth) | **POST** /enterprise/auth |  |



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
  const api = new EnterpriseApi();

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

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

