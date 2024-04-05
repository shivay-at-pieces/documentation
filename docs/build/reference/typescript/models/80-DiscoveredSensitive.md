
# DiscoveredSensitive

This will return a discoveredSensitive, with a seed that can be used to create if automatic is set to false. and will provide the original text provided.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**schema** | [**EmbeddedModelSchema**](EmbeddedModelSchema) |  | [optional] [default to undefined]
**seed** | [**SeededSensitive**](SeededSensitive) |  | [default to undefined]
**text** | **string** |  | [default to undefined]

## Example

```typescript
import { DiscoveredSensitive } from '';

// TODO: Update the object below with actual values
const example: DiscoveredSensitive = {
    "schema": null, // 
    "seed": null, // 
    "text": null, // 
};

console.log(example);

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example);
console.log(exampleJSON);

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as DiscoveredSensitive;
console.log(exampleParsed);
```



