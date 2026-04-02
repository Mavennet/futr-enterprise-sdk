
# ImportClientsDTO


## Properties

Name | Type
------------ | -------------
`clients` | [Array&lt;ImportClientDTO&gt;](ImportClientDTO.md)

## Example

```typescript
import type { ImportClientsDTO } from ''

// TODO: Update the object below with actual values
const example = {
  "clients": [{"clientEmail":"client1@example.com","clientId":"client_001"},{"clientEmail":"client2@example.com","clientId":"client_002"}],
} satisfies ImportClientsDTO

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as ImportClientsDTO
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


