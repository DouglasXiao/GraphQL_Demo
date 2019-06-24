GRAPHQL DEMO SITE
=====================

A wrapper around [SWAPI](http://swapi.co) built using GraphQL converting it into [this schema](schema.graphql).

Uses:

* [graphql-js](https://github.com/graphql/graphql-js) - a JavaScript GraphQL runtime.
* [DataLoader](https://github.com/facebook/dataloader) - for coalescing and caching fetches.
* [express-graphql](https://github.com/graphql/express-graphql) - to provide HTTP access to GraphQL.
* [GraphiQL](https://github.com/graphql/graphiql) - for easy exploration of this GraphQL server.

## Getting Started

Install dependencies with

```sh
npm install
```

## Local Server

A local express server is in `./server`. It can be run with:

```sh
npm run build
npm run start
```

A GraphiQL instance will be opened at http://localhost:xxxx/ (the actual port number will be printed to the console) to explore the API.
