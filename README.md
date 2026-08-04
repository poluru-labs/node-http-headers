# node-http-headers

A lightweight Node.js module for managing common HTTP response headers in Express applications. It helps you add consistent CORS and JSON response settings with minimal setup.

## Uses

Use this module when you want to:

- add default CORS headers to your API routes
- standardize JSON response headers across requests
- simplify header setup for local development and browser-based clients
- keep header logic reusable in one place

Example:

```js
const express = require('express');
const HttpHeader = require('./http');

const app = express();
app.use(HttpHeader.setDefaultHeaders);

app.get('/', (req, res) => {
  res.json({ message: 'Hello from node-http-headers' });
});
```

## Why

HTTP headers are essential for API reliability and browser compatibility. This module makes it easier to manage common settings such as allowed origins, methods, credentials, and content type without repeating the same code in every route.

## Advantages

- simple and easy to integrate into Express apps
- centralizes header configuration for cleaner code
- supports common CORS requirements out of the box
- reduces boilerplate for JSON API responses
- lightweight and focused on a single responsibility

## Navigation

- [Example usage](example.js)
- [HTTP header module](http.js)
- [Package metadata](package.json)
