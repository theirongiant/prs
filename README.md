# Personal React Starter
Step-by-step React setup

### [Initial Commit](https://github.com/theirongiant/prs/commit/e50cbbb49a7fd4643818418090b332828279389b)

Added README.md

### [Add gitignore](https://github.com/theirongiant/prs/commit/83769f302132d4bd9d8b1a7b23ba83a5a9525e6b)

Ran `npm init` to create package.json

Added .gitignore to ignore the node_modules folder

node_modules is huge and can be rebuilt from the dependencies in package.json by running `npm install`

### [Install React/ReactDom](https://github.com/theirongiant/prs/commit/46148c50bb560aeb1157020ce2fafecc65a64bf5)

Ran `npm install --save react react-dom`

React is split into the core library and a number of different renderers, react-dom is what we'll use for web apps but there are other options like react-native for mobile.

### [Install Webpack](https://github.com/theirongiant/prs/commit/0912824c6c21700ebe8e886c1375793d7967e56f)

Ran `npm install --save-dev webpack webpack-cli`

Webpack is a module bundler, with plugins it'll allow us to transpile es6 code into browser friendly es5 and a ton of other things

### [Install Babel](https://github.com/theirongiant/prs/commit/92d56b5653724db589613acc4525a6657432fdb8)

Ran `npm install --save-dev @babel/core babel-loader @babel/preset-env @babel/preset-react`

Babel does the transpiling for us, the two presets will allow webpack to use the loader to work with es6 and react.

.babelrc is where we configure what plugins we want babel to use.

NOTE: Previous version of babel (< v7) would have used `npm install --save -dev babel-core babel-loader babel-preset-env babel-preset-react`
In version 7 they moved the various packages in the @babel scope. [Info on npm scopes](https://docs.npmjs.com/misc/scope)

### [Configure webpack to use babel]()
