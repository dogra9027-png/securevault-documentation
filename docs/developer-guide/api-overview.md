# API Overview

[← Back to Developer Guide](../index.md)

## Overview
The SecureVault API allows applications to interact with the SecureVault document management system. Using the API, developers can upload, share, and delete documents programmatically.

## Base URL
https://api.securevault.example.com/v1

All API requests should use the SecureVault API base URL.

## Authentication

The developer's application sends an API request to SecureVault along with valid authentication credentials, such as an OAuth access token or API key. SecureVault validates the credentials to authenticate the application or user before processing the request. After successful authentication, SecureVault proceeds to authorization checks to determine whether the requester has permission to perform the requested operation.

## Authorization

After the application is authenticated, SecureVault checks the roles and permissions assigned to the user. If a normal user attempts to delete a document, SecureVault returns a `403 Forbidden` response because only administrators are authorized to delete documents.

## Related Topics

- [Authentication](authentication.md)
- [Request and Response Format](request-response-format.md)
- [Error Codes](error-codes.md)
- [Upload a Document](upload-document.md)
- [Delete a Document](delete-document.md)
