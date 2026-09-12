# API Quick Start

## Overview

The API Quick Start provides instructions for developers on how to use the SecureVault API. It guides developers through authentication, making an API request, and reviewing the response.

## Prerequisites

Before using the SecureVault API, developers must have valid API credentials, such as an OAuth access token or API key.

## Authenticate

The developer's application authenticates with SecureVault using a valid OAuth access token or API key. The application includes the credential with the API request so SecureVault can authenticate the requester before processing the request.

## Make an API Request

The application sends an HTTP request to a SecureVault API endpoint. The request includes the required HTTP method, endpoint, authentication credentials, and any required request data.

For example:

```http
GET /documents
Authorization: Bearer <access-token>
```

The `GET /documents` request retrieves documents from SecureVault.

## Review the Response

After processing the request, SecureVault returns an HTTP response. The response includes an HTTP status code that indicates whether the request was successful and may include response headers and a response body.

For example:

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "id": "12345",
  "name": "report.pdf",
  "type": "PDF"
}
```

The `200 OK` status code indicates that the request was successfully processed.

## Next Steps

After completing the Quick Start, developers can explore the available API endpoints. They can learn more about request and response formats, authentication, security requirements, and API error codes.

## Related Topics

- [API Overview](api-overview.md)
- [Authentication](authentication.md)
- [Error Codes](error-codes.md)
- [Upload a Document](upload-document.md)
- [Delete a Document](delete-document.md)
