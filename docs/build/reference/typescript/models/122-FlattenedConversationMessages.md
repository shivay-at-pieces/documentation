
# FlattenedConversationMessages Model

This is a flattened plural version of ConversationMessages

## Properties Model

Name | Type
------------ | -------------
**schema** | [**EmbeddedModelSchema**](EmbeddedModelSchema)
**iterable** | [**Array&lt;ReferencedConversationMessage&gt;**](ReferencedConversationMessage)
**indices** | **\{ [key: string]: number; \}**
**score** | [**Score**](Score)

## Example Model

```typescript
import { FlattenedConversationMessages } from '@pieces.app/pieces-os-client'

// TODO: Update the object below with actual values
const example: FlattenedConversationMessages = {
    "schema": null,
    "iterable": null,
    "indices": null,
    "score": null,
}

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as FlattenedConversationMessages
console.log(exampleParsed)
```

