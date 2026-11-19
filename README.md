# Wild Horizons API

A REST API that provides information about some of the world's most interesting places. The API supports retrieving the full dataset, filtering destinations by query parameters, and accessing destinations by continent or country.

## Features

- Retrieve the complete list of destinations.
- Filter destinations by continent.
- Filter destinations by country.
- Filter destinations by public access status.
- Retrieve destinations by continent or country through dedicated routes.
- JSON responses with appropriate HTTP status codes.
- CORS support.

## Tech Stack

- Node.js
- JavaScript
- Native Node.js HTTP module

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/)

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/thisisniloykhan/wild-horizons-api.git
   ```

2. Navigate to the project directory:

   ```bash
   cd wild-horizons-api
   ```

3. Install dependencies:

   ```bash
   npm install
   ```

4. Start the server:

   ```bash
   npm start
   ```

The API will be available at:

```text
http://localhost:8000
```

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api` | Retrieve all destinations |
| GET | `/api?continent=Asia` | Filter destinations by continent |
| GET | `/api?country=Japan` | Filter destinations by country |
| GET | `/api?is_open_to_public=true` | Filter by public access status |
| GET | `/api/continent/:continent` | Retrieve destinations by continent |
| GET | `/api/country/:country` | Retrieve destinations by country |

Query parameters can also be combined.

Example:

```text
/api?continent=Asia&is_open_to_public=true
```

## Project Structure

```text
wild-horizons-api/
├── data/
│   └── data.js
├── database/
│   └── db.js
├── utils/
│   ├── getDataByPathParams.js
│   ├── getDataByQueryParams.js
│   └── sendJSONResponse.js
├── package.json
├── package-lock.json
└── server.js
```

## Project Background

This project was developed as part of a course to practise building a REST API with Node.js and handling HTTP requests, route parameters, query parameters, and JSON responses.
