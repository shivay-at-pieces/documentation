
# RevokedPKCE Model

A model to support revoking a Token Generated Through PKCE  The behaviour of this endpoint depends on the state of the Refresh Token Revocation Deletes Grant toggle.  If this toggle is enabled, then each revocation request invalidates not only the specific token, but all other tokens based on the same authorization grant.  This means that all Refresh Tokens that have been issued for the same user, application, and audience will be revoked. If this toggle is disabled, then only the refresh token is revoked, while the grant is left intact

## Properties Model

Name | Type
------------ | -------------
**schema** | [**EmbeddedModelSchema**](EmbeddedModelSchema)
**clientId** | **string**
**token** | **string**

## Example Model

```typescript
import { RevokedPKCE } from '@pieces.app/pieces-os-client'

// TODO: Update the object below with actual values
const example: RevokedPKCE = {
    "schema": null,
    "clientId": null,
    "token": null,
}

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as RevokedPKCE
console.log(exampleParsed)
```

