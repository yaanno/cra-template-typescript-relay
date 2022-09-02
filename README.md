# cra-template-typescript-relay

This is an _unofficial_ TypeScript template for [Create React App](https://github.com/facebook/create-react-app) with [Relay](https://relay.dev/) essentials preinstalled.

To use this template, fetch the repository and add `--template file:cra-template-typescript-relay` when creating a new app.

For example, assuming this repo is in your workspace:

```sh
npx create-react-app my-app --template file:cra-template-typescript-relay

# or

yarn create react-app my-app --template file:cra-template-typescript-relay
```

Once your app has been built, update your `package.json` with your `schema` file:

```json
"relay": {
    "language": "typescript",
	"src": "./src/",
	"schema": "./schema.graphql"
  },
```

And for convenience:

```json
"scripts": {
    "start": "yarn run relay && react-scripts start",
    "build": "yarn run relay && react-scripts build",
    "relay": "yarn run relay-compiler",
  }
```

For more information, please refer to:

- [Getting Started](https://create-react-app.dev/docs/getting-started) – How to create a new app.
- [User Guide](https://create-react-app.dev) – How to develop apps bootstrapped with Create React App.
