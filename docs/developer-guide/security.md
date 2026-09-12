# API Security

## Overview
Developers should protect API credentials and use secure communication methods, such as HTTPS, when making requests to SecureVault. Strong authentication and appropriate permissions should also be used to protect API resources.

### Protect API Credentials

Developers should use strong, randomly generated API credentials and avoid credentials that are easy to guess. API keys and access tokens should be stored securely in a protected location, such as a secrets manager or an encrypted configuration file, and should not be exposed in source code.

### Use HTTPS

Developers should use HTTPS when communicating with SecureVault. HTTPS encrypts data transmitted between the application and the API, helping protect credentials and other sensitive information from unauthorized access during transmission.

### Apply Least Privilege

Developers should apply the principle of least privilege by granting users and applications only the permissions required to perform their tasks. SecureVault should verify the requester's identity and permissions before allowing access to resources or operations.

### Authentication and Authorization

SecureVault should authenticate each API request using valid credentials, such as an OAuth access token or API key. After authentication, SecureVault should verify the requester's roles and permissions before allowing access to resources or operations. For example, an authenticated normal user attempting to delete a document receives a `403 Forbidden` response because only administrators are authorized to perform the operation.

### Secure API Requests

Developers can secure API requests by using HTTPS and protecting credentials, such as OAuth access tokens and API keys, by storing them in a secure location.