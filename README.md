[![version](https://img.shields.io/npm/v/runco.svg)]() [![license](https://img.shields.io/github/license/porsager/runco.svg)]()

# `runco`

A very simple no dependencies way to run multiple npm scripts in parallel / concurrently.

It supports wildcards and loads environment variables from your `.env` files automatically.

## Example

This sample will run 
```
{
    "name": "some_npm_package",
    "scripts": {
        "dev:client": "node client/index.js",
        "dev:server": "node server/index.js",
        "dev": "runco dev:*"
    }
}
