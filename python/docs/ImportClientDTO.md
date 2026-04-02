# ImportClientDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**client_email** | **str** | Email address of the client to import | 
**client_id** | **str** | Unique external identifier for the client. Used to track and associate this consumer with your external enterprise system. This ID is stored in the system and can be used for reporting and client tracking purposes. | 

## Example

```python
from openapi_client.models.import_client_dto import ImportClientDTO

# TODO update the JSON string below
json = "{}"
# create an instance of ImportClientDTO from a JSON string
import_client_dto_instance = ImportClientDTO.from_json(json)
# print the JSON string representation of the object
print(ImportClientDTO.to_json())

# convert the object into a dict
import_client_dto_dict = import_client_dto_instance.to_dict()
# create an instance of ImportClientDTO from a dict
import_client_dto_from_dict = ImportClientDTO.from_dict(import_client_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


