
# TrackedKeyboardEvent Model

This is a model that will hold relavent information in relation to a keyboard(including shortcuts) analytics event (usage).

## Properties Model

Name | Type
------------ | -------------
**schema** | [**EmbeddedModelSchema**](EmbeddedModelSchema)
**description** | **string**
**shortcut** | **Array&lt;number&gt;**

## Example Model

```typescript
import { TrackedKeyboardEvent } from '@pieces.app/pieces-os-client'

// TODO: Update the object below with actual values
const example: TrackedKeyboardEvent = {
    "schema": null,
    "description": null,
    "shortcut": null,
}

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as TrackedKeyboardEvent
console.log(exampleParsed)
```

