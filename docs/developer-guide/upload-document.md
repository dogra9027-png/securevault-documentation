# Upload a Document

[← Back to Developer Guide](../index.md)

## Endpoint
An endpoint is a specific URL or path that an API exposes to allow an application or user to access or perform an operation on a resource in SecureVault. 

For this operation:

POST /documents

The POST /documents endpoint uploads a document to SecureVault.

## Authentication

# Upload a Document

The `POST /documents` endpoint allows the developer's application to upload a document to SecureVault.

## Endpoint

An endpoint is a specific URL or path that an API exposes to allow an application or user to access or perform an operation on a resource in SecureVault.

For this operation:

```http
POST /documents
```

The `POST /documents` endpoint uploads a document to SecureVault.

## Authentication

The developer's application sends an API request to SecureVault along with valid authentication credentials, such as an OAuth access token or API key. SecureVault validates the credentials to authenticate the application or user before processing the request.

## Authorization

After the application is authenticated, SecureVault checks the roles and permissions assigned to the user. If a normal user attempts to delete a document, SecureVault returns a `403 Forbidden` response because only administrators are authorized to delete documents.

> **Note:** For the upload operation, SecureVault checks whether the authenticated user has permission to upload a document.

## Request

The request must include the document that needs to be uploaded to SecureVault.

## Response

If the document is uploaded successfully, SecureVault returns:

```http
201 Created
```

The `201 Created` response indicates that the document was successfully uploaded to SecureVault.

## Errors

| Status Code        | Description                                                           |
| ------------------ | --------------------------------------------------------------------- |
| `400 Bad Request`  | The request contains invalid or missing data.                         |
| `401 Unauthorized` | Authentication credentials are missing or invalid.                    |
| `403 Forbidden`    | The authenticated user does not have permission to upload a document. |


## Related Topics

- [Authentication](authentication.md)
- [Request and Response Format](request-response-format.md)
- [Error Codes](error-codes.md)
- [Delete a Document](delete-document.md)