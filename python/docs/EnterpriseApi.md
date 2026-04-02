# openapi_client.EnterpriseApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**enterprise_controller_auth**](EnterpriseApi.md#enterprise_controller_auth) | **POST** /enterprise/auth | Authenticate and retrieve OAuth2 token
[**enterprise_controller_import_clients**](EnterpriseApi.md#enterprise_controller_import_clients) | **POST** /enterprise/import-clients | Import enterprise clients


# **enterprise_controller_auth**
> object enterprise_controller_auth(auth_dto)

Authenticate and retrieve OAuth2 token

Exchanges your enterprise client credentials for an
OAuth2 access token. This token is required for accessing protected
enterprise endpoints including import-clients and document operations.


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
    auth_dto = {"clientId":"abc123xyz789","clientSecret":"secret_key_12345"} # AuthDTO | 

    try:
        # Authenticate and retrieve OAuth2 token
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
**200** | Successfully authenticated. Access token returned with doc/upload scope. |  -  |
**201** |  |  -  |
**401** | Invalid client credentials provided. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **enterprise_controller_import_clients**
> object enterprise_controller_import_clients(import_clients_dto)

Import enterprise clients

Imports a list of clients into your organization. Requires a
valid OAuth2 access token obtained from the /auth endpoint. Each client
will be added to your organization with the provided email and unique
external client ID.

The clientId will serve as an external identifier to track which
enterprise client each consumer belongs to. Critically, this clientId
mapping determines document upload behavior: documents uploaded by
imported clients will be stored unencrypted (enterprise-managed storage).
Clients will be created in Cognito if they do not already exist, and
their association with your organization and the provided clientId will
be stored in the system.

Import Format:
A customer-generated CSV file will be used to onboard multiple users in
bulk. The CSV file will have the following format:

clientEmail,clientId

When using the Brands App, the user's email will be used as the
clientEmail and the initial password will be an OTP sent to the
user's email. The clientId will be any unique identifier from your
enterprise system that you want to associate with this client. This will
allow you to maintain a mapping between your enterprise system and the
consumers created in this platform, and will enable unencrypted document
storage for these clients.



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
    import_clients_dto = {"clients":[{"clientEmail":"client@example.com","clientId":"client_001"}]} # ImportClientsDTO | 

    try:
        # Import enterprise clients
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
**201** | Clients successfully imported. Returns an empty response body. |  -  |
**400** | Invalid request body. Ensure clients array has at least 1 item and all fields are valid. |  -  |
**401** | Unauthorized. Invalid or missing OAuth2 token. |  -  |
**403** | Forbidden. Your organization does not have enterprise access. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

