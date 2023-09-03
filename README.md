# Express API: Who Am I?
This is a simple Node.js application built with the Express.js framework that provides information about the client's IP address, preferred language, and user-agent (browser or device) when they access the `/api/whoami` endpoint.

## Prerequisites
Before running this application, make sure you have the following installed:

- Node.js: [https://nodejs.org/](https://nodejs.org/)
- npm (Node Package Manager): Included with Node.js

## API Endpoint

- **GET /api/whoami**

  When you make a GET request to this endpoint, it will return a JSON response with the following information:

  - `ipaddress`: The client's IP address.
  - `language`: The client's preferred language, extracted from the `Accept-Language` header.
  - `software`: Information about the client's software (user-agent), extracted from the `User-Agent` header.

  Example Response:

  ```json
  {
    "ipaddress": "127.0.0.1",
    "language": "en-US,en;q=0.9",
    "software": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.93 Safari/537.36"
  }

## Configuration
The server listens on the port specified in the process.env.PORT environment variable. If not defined, it defaults to port 3000.
CORS (Cross-Origin Resource Sharing) headers are enabled to allow remote testing of the API.
