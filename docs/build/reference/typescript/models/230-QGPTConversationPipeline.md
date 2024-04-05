
# QGPTConversationPipeline

This model is specifically for QGPT Conversation pipelines, the model is used to group conversational prompts for instance a conversation around generating code.  here are some use cases- 1. contextualized_code_generation- This is for users that want to have conversations around generating code, when there is provided context. 2. generalized_code- This is for users that want to have conversations without context around code. 3. contextualized_code- This is for users that want to have conversation around code with Context.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**schema** | [**EmbeddedModelSchema**](EmbeddedModelSchema) |  | [optional] [default to undefined]
**contextualizedCodeGeneration** | [**QGPTConversationPipelineForContextualizedCodeGeneration**](QGPTConversationPipelineForContextualizedCodeGeneration) |  | [optional] [default to undefined]
**generalizedCodeDialog** | [**QGPTConversationPipelineForGeneralizedCodeDialog**](QGPTConversationPipelineForGeneralizedCodeDialog) |  | [optional] [default to undefined]
**contextualizedCodeDialog** | [**QGPTConversationPipelineForContextualizedCodeDialog**](QGPTConversationPipelineForContextualizedCodeDialog) |  | [optional] [default to undefined]

## Example

```typescript
import { QGPTConversationPipeline } from '';

// TODO: Update the object below with actual values
const example: QGPTConversationPipeline = {
    "schema": null, // 
    "contextualizedCodeGeneration": null, // 
    "generalizedCodeDialog": null, // 
    "contextualizedCodeDialog": null, // 
};

console.log(example);

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example);
console.log(exampleJSON);

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as QGPTConversationPipeline;
console.log(exampleParsed);
```



