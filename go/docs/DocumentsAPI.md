# \DocumentsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**DocumentControllerUploadDocument**](DocumentsAPI.md#DocumentControllerUploadDocument) | **Post** /documents | Uploading a new document



## DocumentControllerUploadDocument

> string DocumentControllerUploadDocument(ctx).File(file).Monetized(monetized).FileHash(fileHash).DerivedKey(derivedKey).Password(password).IsID(isID).TaskId(taskId).Execute()

Uploading a new document

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/GIT_USER_ID/GIT_REPO_ID"
)

func main() {
	file := os.NewFile(1234, "some_file") // *os.File | 
	monetized := true // bool | 
	fileHash := "fileHash_example" // string | 
	derivedKey := "derivedKey_example" // string | required for end-client use only, enterprise should skip this property (optional)
	password := "password_example" // string | user's decryption password (optional)
	isID := true // bool |  (optional)
	taskId := "taskId_example" // string |  (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.DocumentsAPI.DocumentControllerUploadDocument(context.Background()).File(file).Monetized(monetized).FileHash(fileHash).DerivedKey(derivedKey).Password(password).IsID(isID).TaskId(taskId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `DocumentsAPI.DocumentControllerUploadDocument``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DocumentControllerUploadDocument`: string
	fmt.Fprintf(os.Stdout, "Response from `DocumentsAPI.DocumentControllerUploadDocument`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiDocumentControllerUploadDocumentRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | ***os.File** |  | 
 **monetized** | **bool** |  | 
 **fileHash** | **string** |  | 
 **derivedKey** | **string** | required for end-client use only, enterprise should skip this property | 
 **password** | **string** | user&#39;s decryption password | 
 **isID** | **bool** |  | 
 **taskId** | **string** |  | 

### Return type

**string**

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

