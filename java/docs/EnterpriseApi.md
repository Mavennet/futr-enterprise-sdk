# EnterpriseApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**enterpriseControllerAuth**](EnterpriseApi.md#enterpriseControllerAuth) | **POST** /enterprise/auth |  |
| [**enterpriseControllerImportClients**](EnterpriseApi.md#enterpriseControllerImportClients) | **POST** /enterprise/import-clients |  |


<a id="enterpriseControllerAuth"></a>
# **enterpriseControllerAuth**
> Object enterpriseControllerAuth(authDTO)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EnterpriseApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    EnterpriseApi apiInstance = new EnterpriseApi(defaultClient);
    AuthDTO authDTO = new AuthDTO(); // AuthDTO | 
    try {
      Object result = apiInstance.enterpriseControllerAuth(authDTO);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EnterpriseApi#enterpriseControllerAuth");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **authDTO** | [**AuthDTO**](AuthDTO.md)|  | |

### Return type

**Object**

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** |  |  -  |

<a id="enterpriseControllerImportClients"></a>
# **enterpriseControllerImportClients**
> Object enterpriseControllerImportClients(importClientsDTO)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EnterpriseApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    EnterpriseApi apiInstance = new EnterpriseApi(defaultClient);
    ImportClientsDTO importClientsDTO = new ImportClientsDTO(); // ImportClientsDTO | 
    try {
      Object result = apiInstance.enterpriseControllerImportClients(importClientsDTO);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EnterpriseApi#enterpriseControllerImportClients");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **importClientsDTO** | [**ImportClientsDTO**](ImportClientsDTO.md)|  | |

### Return type

**Object**

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** |  |  -  |

