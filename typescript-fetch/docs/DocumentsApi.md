# DocumentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**documentControllerUploadDocument**](DocumentsApi.md#documentcontrolleruploaddocument) | **POST** /documents | Uploading a new document |



## documentControllerUploadDocument

> string documentControllerUploadDocument(file, monetized, fileHash, derivedKey, password, isID, taskId)

Uploading a new document

### Example

```ts
import {
  Configuration,
  DocumentsApi,
} from '';
import type { DocumentControllerUploadDocumentRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearer
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new DocumentsApi(config);

  const body = {
    // Blob
    file: BINARY_DATA_HERE,
    // boolean
    monetized: true,
    // string
    fileHash: fileHash_example,
    // string | required for end-client use only, enterprise should skip this property (optional)
    derivedKey: derivedKey_example,
    // string | user\\\'s decryption password (optional)
    password: password_example,
    // boolean (optional)
    isID: true,
    // string (optional)
    taskId: taskId_example,
  } satisfies DocumentControllerUploadDocumentRequest;

  try {
    const data = await api.documentControllerUploadDocument(body);
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
| **file** | `Blob` |  | [Defaults to `undefined`] |
| **monetized** | `boolean` |  | [Defaults to `undefined`] |
| **fileHash** | `string` |  | [Defaults to `undefined`] |
| **derivedKey** | `string` | required for end-client use only, enterprise should skip this property | [Optional] [Defaults to `undefined`] |
| **password** | `string` | user\\\&#39;s decryption password | [Optional] [Defaults to `undefined`] |
| **isID** | `boolean` |  | [Optional] [Defaults to `undefined`] |
| **taskId** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

**string**

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

