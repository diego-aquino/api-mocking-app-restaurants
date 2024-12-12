# Restaurant Search - Applying API Mocks

This application allows you to search for highly rated restaurants around the
world using the
[Google Maps Places API](https://developers.google.com/maps/documentation/places/web-service).

## 1. Access

[![Open in Stackblitz](https://developer.stackblitz.com/img/open_in_stackblitz.svg)](https://stackblitz.com/github/diego-aquino/api-mocking-app-restaurants?startScript=dev&file=README.md)

## 2. Project

Important files:

- [`src/server/app.ts`](./src/server/app.ts): main application file, where the
  server is implemented.
- [`src/clients/GoogleMapsPlacesClient.ts`](./src/clients/googleMaps/GoogleMapsPlacesClient.ts):
  class that makes HTTP calls to the Places API.
- [`tests/restaurants.test.ts`](./tests/restaurants.test.ts): file for
  restaurant search tests.

Useful commands:

- `npm install`: installs the project's **dependencies**.
- `npm run dev`: starts the **server** in development mode.
- `npm run test`: runs the application's **tests** in watch mode.
- `npm run types:check`: checks for **type errors** in the code.

Mock tools:

- **MSW**: https://github.com/mswjs/msw
- **Zimic**: https://github.com/zimicjs/zimic/wiki

## 3. Google Maps Places API

- OpenAPI Documentation:
  - Current version:
    [`openapi.yaml`](https://gist.githubusercontent.com/diego-aquino/21b772332f2455a827166ac3b64db052/raw/b9aed7f76a91bf216cee5fb37fe2fd1e0d959c80/google-maps-places-api-current.openapi.yaml)
    ([View in Swagger UI](https://editor-next.swagger.io/?url=https://gist.githubusercontent.com/diego-aquino/21b772332f2455a827166ac3b64db052/raw/b9aed7f76a91bf216cee5fb37fe2fd1e0d959c80/))

### 3.1. Text Search

- [Documentation](https://developers.google.com/maps/documentation/places/web-service/search-text)
  - [Status](https://developers.google.com/maps/documentation/places/web-service/search-text#PlacesSearchStatus)

Request examples:

- Success
  ```bash
  npm run example current success
  ```
- Failure
  ```bash
  npm run example current error
  ```

### 3.2. Text Search (New)

- [Documentation](https://developers.google.com/maps/documentation/places/web-service/text-search)
- [Migration guide](https://developers.google.com/maps/documentation/places/web-service/migrate-text)

Request examples:

- Success
  ```bash
  npm run example new success
  ```
- Failure
  ```bash
  npm run example new error
  ```
