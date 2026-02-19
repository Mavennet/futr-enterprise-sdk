
# AuthDTO


## Properties

Name | Type
------------ | -------------
`clientId` | string
`clientSecret` | string

## Example

```typescript
import type { AuthDTO } from ''

// TODO: Update the object below with actual values
const example = {
  "clientId": null,
  "clientSecret": null,
} satisfies AuthDTO

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as AuthDTO
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


