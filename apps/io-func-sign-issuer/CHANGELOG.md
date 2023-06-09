# io-func-sign-issuer

## 0.11.0

### Minor Changes

- c5e2774: Added self-care integration
- 76f46cc: Added health-check on the whole infra. [SFEQS-1273]
  `makeFetchWithTimeout` has been moved to the `io-sign` package.
- 7cc0178: Add CreateIssuerByVatNumberView function, triggered by cosmos db to create a lookup table to obtain issuers by their vatNumber
- e6a3334: BREAKING CHANGE: Added `formFields` attribute to `DocumentMetadata` in `io-sign` package
  [SFEQS-1266] Added validation of signature fields and pages during `ValidateUpload` in `io-func-sign-issuer`
  [SFEQS-1216] Fixed infra dependencies
- 5481a80: Require at least one mandatory signature for each dossier
- a0a818d: expand signature request to include issuer e-mail and description
- 2e646fd: Added billing event
- 1794895: Add functions to sync Signature Request statuses across the system

### Patch Changes

- 045b0eb: Added third_party_data to notification
- e456d1b: - Added headers required by lollipop to `createSignature`
  - Added lollipop infrastructure for API access
  - Added SPID assertion retrieval via lollipop API
  - Implemented forwarding of parameters to QTSP
- 0c3c3a7: Change the leaseCollectionName and add leaseCollectionPrefix to CreateIssuerByVatNumber
- 3e00bff: Notification send refactor
  [SFEQS-1323,1329] Fixed sent notification messages
  [SFEQS-1325] Bug fix on updatedAt field
  [SFEQS-1311] Bug fix multiple notifications
- 7469d10: Make "signature_fields" field optional in rest APIs
- 6a3d7b6: fix minor bugs on REST API serialization and error responses
- f5b5f67: Patch signature notification message
- ec71e65: pre-authenticate urls on signed signature requests (issuer)
- 072f30f: Change extensionBundle
- 20d5692: Updated notification message text
- d1f4f7e: Set maxPollingInterval for queues to 5 seconds
- fc69f72: Changed notification message
- 8afb588: Moved `getDocument` and `SignatureRequestDraft` to @io-sign package
- 7a0612d: Split analytics and billing event hubs
- Updated dependencies [045b0eb]
- Updated dependencies [c5e2774]
- Updated dependencies [e456d1b]
- Updated dependencies [12100f7]
- Updated dependencies [76f46cc]
- Updated dependencies [7cc0178]
- Updated dependencies [3e00bff]
- Updated dependencies [e6a3334]
- Updated dependencies [6a3d7b6]
- Updated dependencies [5481a80]
- Updated dependencies [78ae07d]
- Updated dependencies [a0a818d]
- Updated dependencies [ec71e65]
- Updated dependencies [22fee87]
- Updated dependencies [62f8a61]
- Updated dependencies [8afb588]
- Updated dependencies [8afb588]
- Updated dependencies [2e646fd]
  - @io-sign/io-sign@1.0.0

## 0.10.0

### Minor Changes

- deb99dd: [SFEQS-1204, SFEQS-1214] Implement `CreateSignatureRequest`, `GetSignatureRequest`, `MarkAsWaitForSignature` Azure Functions

### Patch Changes

- c4952ec: GetSignatureRequest now serialize the correct attributes for each document status [SFEQS-1141]
- Updated dependencies [336cd7a]
- Updated dependencies [deb99dd]
  - @io-sign/io-sign@0.9.0
