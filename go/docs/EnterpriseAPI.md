# \EnterpriseAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**EnterpriseControllerAuth**](EnterpriseAPI.md#EnterpriseControllerAuth) | **Post** /enterprise/auth | 



## EnterpriseControllerAuth

> map[string]interface{} EnterpriseControllerAuth(ctx).AuthDTO(authDTO).Execute()



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
	authDTO := *openapiclient.NewAuthDTO("ClientId_example", "ClientSecret_example") // AuthDTO | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.EnterpriseAPI.EnterpriseControllerAuth(context.Background()).AuthDTO(authDTO).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `EnterpriseAPI.EnterpriseControllerAuth``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `EnterpriseControllerAuth`: map[string]interface{}
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

**map[string]interface{}**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

