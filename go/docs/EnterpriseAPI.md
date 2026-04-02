# \EnterpriseAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**EnterpriseControllerAuth**](EnterpriseAPI.md#EnterpriseControllerAuth) | **Post** /enterprise/auth | Authenticate and retrieve OAuth2 token
[**EnterpriseControllerImportClients**](EnterpriseAPI.md#EnterpriseControllerImportClients) | **Post** /enterprise/import-clients | Import enterprise clients



## EnterpriseControllerAuth

> interface{} EnterpriseControllerAuth(ctx).AuthDTO(authDTO).Execute()

Authenticate and retrieve OAuth2 token



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
	authDTO := *openapiclient.NewAuthDTO("abc123xyz789", "secret_key_12345") // AuthDTO | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.EnterpriseAPI.EnterpriseControllerAuth(context.Background()).AuthDTO(authDTO).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `EnterpriseAPI.EnterpriseControllerAuth``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `EnterpriseControllerAuth`: interface{}
	fmt.Fprintf(os.Stdout, "Response from `EnterpriseAPI.EnterpriseControllerAuth`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiEnterpriseControllerAuthRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authDTO** | [**AuthDTO**](AuthDTO.md) |  | 

### Return type

**interface{}**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## EnterpriseControllerImportClients

> interface{} EnterpriseControllerImportClients(ctx).ImportClientsDTO(importClientsDTO).Execute()

Import enterprise clients



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
	importClientsDTO := *openapiclient.NewImportClientsDTO([]openapiclient.ImportClientDTO{*openapiclient.NewImportClientDTO("client@example.com", "client_001")}) // ImportClientsDTO | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.EnterpriseAPI.EnterpriseControllerImportClients(context.Background()).ImportClientsDTO(importClientsDTO).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `EnterpriseAPI.EnterpriseControllerImportClients``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `EnterpriseControllerImportClients`: interface{}
	fmt.Fprintf(os.Stdout, "Response from `EnterpriseAPI.EnterpriseControllerImportClients`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiEnterpriseControllerImportClientsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **importClientsDTO** | [**ImportClientsDTO**](ImportClientsDTO.md) |  | 

### Return type

**interface{}**

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

