# openapi_client.EnterpriseApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**enterprise_controller_auth**](EnterpriseApi.md#enterprise_controller_auth) | **POST** /enterprise/auth | 
[**enterprise_controller_import_clients**](EnterpriseApi.md#enterprise_controller_import_clients) | **POST** /enterprise/import-clients | 


# **enterprise_controller_auth**
> object enterprise_controller_auth(auth_dto)

### Example

* Bearer (JWT) Authentication (bearer):

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

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): bearer
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
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

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **enterprise_controller_import_clients**
> object enterprise_controller_import_clients(import_clients_dto)

### Example

* Bearer (JWT) Authentication (bearer):

```python
import openapi_client
from openapi_client.models.import_clients_dto import ImportClientsDTO
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): bearer
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.EnterpriseApi(api_client)
    import_clients_dto = openapi_client.ImportClientsDTO() # ImportClientsDTO | 

    try:
        api_response = api_instance.enterprise_controller_import_clients(import_clients_dto)
        print("The response of EnterpriseApi->enterprise_controller_import_clients:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EnterpriseApi->enterprise_controller_import_clients: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **import_clients_dto** | [**ImportClientsDTO**](ImportClientsDTO.md)|  | 

### Return type

**object**

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

