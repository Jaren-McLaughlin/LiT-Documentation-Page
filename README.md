# Docs Site

This site is built with [Docusaurus](https://docusaurus.io/) and hosts project docs plus generated API references.

## Install

From this directory:

```bash
npm install
```

## Local development

```bash
npm start
```

## Build

```bash
npm run build
```

## Regenerate API docs

From the repository root:

```bash
node scripts/generateDocs.js
```

Generated static API docs are placed in:

`scripts/docs-site/static/api`

Current generators:
- JavaScript: JSDoc
- Java: Gradle Javadoc
- Python: pdoc (optional, requires `python3 -m pip install pdoc`)
