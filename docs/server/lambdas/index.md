# Lambda Services

This directory contains the AWS Lambda code for backend API endpoints.

## Docs

- [API docs for Java Lambda code](./api.md)

## Structure

- `src/main/java/lambda/login`: login/logout handlers and request/response models
- `src/main/java/lambda/session`: create/join/leave/delete session handlers and models
- `src/main/java/util`: shared utility helpers used by lambdas
- `shared`: shared library module used by the main lambda module

## Build

From this directory:

```bash
./gradlew build
```

Generate Javadocs:

```bash
./gradlew javadoc
```

Output is written to:

`build/docs/javadoc`