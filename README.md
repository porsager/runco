[![version](https://img.shields.io/npm/v/runco.svg)]() [![license](https://img.shields.io/github/license/porsager/runco.svg)]()

# `runco`

A very simple no dependencies way to run multiple npm scripts in parallel / concurrently.

It supports tail wildcards and loads environment variables from `.env` files automatically.

It also allows child processes to gracefully exit on SIGINT which helps when testing things that need a shutdown procedure.

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
