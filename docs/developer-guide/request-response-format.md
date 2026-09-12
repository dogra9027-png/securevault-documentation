# Request and Response Format

[← Back to Developer Guide](../index.md)

## Overview

An HTTP request contains an HTTP method, endpoint, headers, parameters, and a request body. 
An HTTP response is returned by the API after processing the request. It contains a status code and may include response data or error information.

## HTTP Request

```http
POST /dcuments
Authorization: Bearer <access-token>
Content-Type: application/json

{
  "name": "report.pdf"
}
```
```http
POST                         → HTTP method

/documents                   → Endpoint

Authorization               → Header

Content-Type                → Header

JSON object                 → Request body
```

### HTTP Method

An HTTP method specifies the type of operation the client wants to perform on a resource. Common HTTP methods include `GET`, `POST`, `PUT`, `PATCH`, and `DELETE`.


### Endpoint

An endpoint is a specific URL or path used to access a SecureVault resource or perform an operation on that resource through an API request.

### Headers
An HTTP header provides additional information about the request, such as authentication credentials and the content type of the request body.

### Parameters 
Parameters are variable values used to provide additional information to an API request, such as a documentId or search keyword.

### Request Body
A request body contains the data sent to the API and can use different formats, such as JSON or form data.

## HTTP Response

```http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": "12345",
  "name": "report.pdf",
  "type": "PDF"
}
```

```http
201 Created                  → Status code
Content-Type                → Response header
JSON object                 → Response body
```

 ### Status Code
A status code is part of an HTTP response. It indicates the result of the API request and can include codes such as 200, 201, 400, 404, and 500.

 ```http
200 → Request successful
201 → Resource created
400 → Invalid request
404 → Resource not found
500 → Server error

```


### Response Header
Response headers provide additional information about the HTTP response, such as the content type, caching information, and server details.

### Response Body
A response body contains the data returned by the API in response to the request. The response body can contain information about the requested resource or the result of the requested operation.

## Related Topics

- [API Overview](api-overview.md)
- [Authentication](authentication.md)
- [Error Codes](error-codes.md)
- [Upload a Document](upload-document.md)
- [Delete a Document](delete-document.md)

