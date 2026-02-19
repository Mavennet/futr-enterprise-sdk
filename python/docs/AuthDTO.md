# AuthDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**client_id** | **str** |  | 
**client_secret** | **str** |  | 

## Example

```python
from openapi_client.models.auth_dto import AuthDTO

# TODO update the JSON string below
json = "{}"
# create an instance of AuthDTO from a JSON string
auth_dto_instance = AuthDTO.from_json(json)
# print the JSON string representation of the object
print(AuthDTO.to_json())

# convert the object into a dict
auth_dto_dict = auth_dto_instance.to_dict()
# create an instance of AuthDTO from a dict
auth_dto_from_dict = AuthDTO.from_dict(auth_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


