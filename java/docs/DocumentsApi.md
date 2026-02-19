# DocumentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**documentControllerUploadDocument**](DocumentsApi.md#documentControllerUploadDocument) | **POST** /documents | Uploading a new document |


<a id="documentControllerUploadDocument"></a>
# **documentControllerUploadDocument**
> String documentControllerUploadDocument(_file, monetized, fileHash, derivedKey, password, isID, taskId)

Uploading a new document

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DocumentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    DocumentsApi apiInstance = new DocumentsApi(defaultClient);
    File _file = new File("/path/to/file"); // File | 
    Boolean monetized = true; // Boolean | 
    String fileHash = "fileHash_example"; // String | 
    String derivedKey = "derivedKey_example"; // String | required for end-client use only, enterprise should skip this property
    String password = "password_example"; // String | user's decryption password
    Boolean isID = true; // Boolean | 
    String taskId = "taskId_example"; // String | 
    try {
      String result = apiInstance.documentControllerUploadDocument(_file, monetized, fileHash, derivedKey, password, isID, taskId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#documentControllerUploadDocument");
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
| **_file** | **File**|  | |
| **monetized** | **Boolean**|  | |
| **fileHash** | **String**|  | |
| **derivedKey** | **String**| required for end-client use only, enterprise should skip this property | [optional] |
| **password** | **String**| user&#39;s decryption password | [optional] |
| **isID** | **Boolean**|  | [optional] |
| **taskId** | **String**|  | [optional] |

### Return type

**String**

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** |  |  -  |

