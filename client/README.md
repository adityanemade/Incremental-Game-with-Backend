# Incremental Game Starter

Welcome to the incremental game starter kit. In this README, we will go over all
the information you need to start hacking!

## Get started

We are using WebpackJS as bundler and BabelJS as transpiler to compile our ES6
JavaScript code down to browser usable JavaScript code.

```
npm run build
```

## Developing

Before start developing, it's important to know the folder structure:

```
[I] ✦ ➜ tree -L 2 -I 'node_modules|package-*'
.
├── README.md
├── index.html                        --> your game index file
├── app.css                           --> your custom styling
├── package.json                      --> dependencies, npm scripts
├── src                               --> where your JavaScript source code is
│   ├── app.js                        --> entry point of whole file
│   ├── constants.js                  --> any constants like growth ratio
│   ├── game.js                       --> background game loop
│   ├── models                        --> Business model (Plain old JavaScript object)
│   │   ├── generator.js              --> Generator business model
│   │   └── story.js                  --> Story business model
│   ├── reducer.js                    --> reducers are for state mutation
│   ├── store.js                      --> simple redux implementation store
│   └── views                         --> all web components lives here
│       ├── example.js                --> For example references
│       ├── generator.js              --> To display generator component
│       └── story-book.js             --> To display story/event component
├── test                              --> where test lives under
└── webpack.config.js                 --> bundler configuration
```

### Prerequisites

Once knowing the folder structure, you will need to install [Node.js](https://nodejs.org/en/).

### Setting up Dev

To set up development environment, you will need to run the following:

```
npm install && npm run build
```

And open up `index.html` under the root directory.

## Test

You can run test through `npm test`.

> In addition to the local testing, TravisCI should be configured so that all the
> tests should be running automatically on every commit
