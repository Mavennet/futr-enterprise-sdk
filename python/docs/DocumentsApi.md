# openapi_client.DocumentsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**document_controller_upload_document**](DocumentsApi.md#document_controller_upload_document) | **POST** /documents | Uploading a new document


# **document_controller_upload_document**
> str document_controller_upload_document(file, monetized, file_hash, derived_key=derived_key, password=password, is_id=is_id, task_id=task_id)

Uploading a new document

### Example

* Bearer (JWT) Authentication (bearer):

```python
import openapi_client
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
    api_instance = openapi_client.DocumentsApi(api_client)
    file = None # bytearray | 
    monetized = True # bool | 
    file_hash = 'file_hash_example' # str | 
    derived_key = 'derived_key_example' # str | required for end-client use only, enterprise should skip this property (optional)
    password = 'password_example' # str | user's decryption password (optional)
    is_id = True # bool |  (optional)
    task_id = 'task_id_example' # str |  (optional)

    try:
        # Uploading a new document
        api_response = api_instance.document_controller_upload_document(file, monetized, file_hash, derived_key=derived_key, password=password, is_id=is_id, task_id=task_id)
        print("The response of DocumentsApi->document_controller_upload_document:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DocumentsApi->document_controller_upload_document: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | **bytearray**|  | 
 **monetized** | **bool**|  | 
 **file_hash** | **str**|  | 
 **derived_key** | **str**| required for end-client use only, enterprise should skip this property | [optional] 
 **password** | **str**| user&#39;s decryption password | [optional] 
 **is_id** | **bool**|  | [optional] 
 **task_id** | **str**|  | [optional] 

### Return type

**str**

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

