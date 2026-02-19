# openapi_client.EnterpriseApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**enterprise_controller_auth**](EnterpriseApi.md#enterprise_controller_auth) | **POST** /enterprise/auth | 


# **enterprise_controller_auth**
> object enterprise_controller_auth(auth_dto)

### Example


```python
import openapi_client
from openapi_client.models.auth_dto import AuthDTO
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.EnterpriseApi(api_client)
    auth_dto = openapi_client.AuthDTO() # AuthDTO | 

    try:
        api_response = api_instance.enterprise_controller_auth(auth_dto)
        print("The response of EnterpriseApi->enterprise_controller_auth:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EnterpriseApi->enterprise_controller_auth: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **auth_dto** | [**AuthDTO**](AuthDTO.md)|  | 

### Return type

**object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

