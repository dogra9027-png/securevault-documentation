# Delete a Document

[← Back to Developer Guide](../index.md)

The `DELETE /documents/{documentId}` endpoint allows the developer's application to delete a document from SecureVault.

## Endpoint

An endpoint is a specific URL or path that an API exposes to allow an application or user to access or perform an operation on a resource in SecureVault.

For this operation:

```http
DELETE /documents/{documentId}
```

The `DELETE /documents/{documentId}` endpoint deletes the specified document from SecureVault.

## Authentication

The developer's application sends an API request to SecureVault along with valid authentication credentials, such as an OAuth access token or API key. SecureVault validates the credentials to authenticate the application or user before processing the request.

## Authorization

After the requester is authenticated, SecureVault checks the roles and permissions assigned to the user. If a normal user attempts to delete a document, SecureVault returns a `403 Forbidden` response because only administrators are authorized to delete documents.

> **Note:** For the delete operation, SecureVault checks whether the authenticated user has permission to delete the document.

## Request

The request must include the `documentId` of the document that needs to be deleted from SecureVault.

## Response

If the document is deleted successfully, SecureVault returns:

```http
204 No Content
```

The `204 No Content` response indicates that the document was successfully deleted from SecureVault.

## Errors

| Status Code        | Description                                                             |
| ------------------ | ----------------------------------------------------------------------- |
| `400 Bad Request`  | The request contains invalid or missing data.                           |
| `401 Unauthorized` | Authentication credentials are missing or invalid.                      |
| `403 Forbidden`    | The authenticated user does not have permission to delete the document. |
| `404 Not Found`    | The specified document could not be found.                              |

## Related Topics

- [Authentication](authentication.md)
- [Request and Response Format](request-response-format.md)
- [Error Codes](error-codes.md)
- [Upload a Document](upload-document.md)