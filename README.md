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
In version 7 they moved the various packages in the @babel scope, essentially this is just an 

[Info on npm scopes](https://docs.npmjs.com/misc/scope)

### [Configure webpack to use babel](https://github.com/theirongiant/prs/commit/8a6f2e5550f07d4707dd381656e5f789603785ca)

Added a webpack.connfig.js file in which we set up a rule telling webpack that if it finds any .js files to process them with the babel-loader before bundling. Also make sure we exclude the node_mondules directory.

Then we added a simple Hello World! react script. 

An addition was made to the package.json scripts section `"build": "webpack --mode production`
When we run this with `npm run build` it will transpile and build our code according to the rules in webpack.config.js and put the resulting bundle in dist/ as main.js

We lastly added the dist/ folder to our gitignore.

