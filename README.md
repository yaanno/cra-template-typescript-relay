# cra-template-typescript-relay

This is an _unofficial_ TypeScript template for [Create React App](https://github.com/facebook/create-react-app) with [Relay](https://relay.dev/) essentials preinstalled.

To use this template run:

```sh
npx create-react-app my-app --template git+https://github.com/yaanno/cra-template-typescript-relay.git

# or

yarn create react-app my-app --template git+https://github.com/yaanno/cra-template-typescript-relay.git
```

Once your app has been built, update your `package.json` with your `schema` file:

```json
"relay": {
  "language": "typescript",
	"src": "./src/",
	"schema": "./schema.graphql"
  },
```

Make Relay available for scripting:

```json
"scripts": {
    "start": "yarn run relay && react-scripts start",
    "build": "yarn run relay && react-scripts build",
    "relay": "yarn run relay-compiler",
  }
```

Relay + React + TypeScript specific "issues" handled by:

- `template/.babelrc`: making sure Babel understands Relay
- `template/src/react-app.d.ts`: making sure `graphql` type system is available via import

A test schema added for convenience

For more information, please refer to:

- [Getting Started](https://create-react-app.dev/docs/getting-started) – How to create a new app.
- [User Guide](https://create-react-app.dev) – How to develop apps bootstrapped with Create React App.
