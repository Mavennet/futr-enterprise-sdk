# ImportClientsDTO

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Clients** | [**[]ImportClientDTO**](ImportClientDTO.md) | Array of clients to import. Each client is identified by their email and a unique external ID from your enterprise system. The external ID (clientId) is used to maintain a mapping between your enterprise system and the consumers created in this platform. Minimum 1 client required. | 

## Methods

### NewImportClientsDTO

`func NewImportClientsDTO(clients []ImportClientDTO, ) *ImportClientsDTO`

NewImportClientsDTO instantiates a new ImportClientsDTO object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewImportClientsDTOWithDefaults

`func NewImportClientsDTOWithDefaults() *ImportClientsDTO`

NewImportClientsDTOWithDefaults instantiates a new ImportClientsDTO object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetClients

`func (o *ImportClientsDTO) GetClients() []ImportClientDTO`

GetClients returns the Clients field if non-nil, zero value otherwise.

### GetClientsOk

`func (o *ImportClientsDTO) GetClientsOk() (*[]ImportClientDTO, bool)`

GetClientsOk returns a tuple with the Clients field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetClients

`func (o *ImportClientsDTO) SetClients(v []ImportClientDTO)`

SetClients sets Clients field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


