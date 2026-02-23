# ImportClientsDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**clients** | [**List[ImportClientDTO]**](ImportClientDTO.md) |  | 

## Example

```python
from openapi_client.models.import_clients_dto import ImportClientsDTO

# TODO update the JSON string below
json = "{}"
# create an instance of ImportClientsDTO from a JSON string
import_clients_dto_instance = ImportClientsDTO.from_json(json)
# print the JSON string representation of the object
print(ImportClientsDTO.to_json())

# convert the object into a dict
import_clients_dto_dict = import_clients_dto_instance.to_dict()
# create an instance of ImportClientsDTO from a dict
import_clients_dto_from_dict = ImportClientsDTO.from_dict(import_clients_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


