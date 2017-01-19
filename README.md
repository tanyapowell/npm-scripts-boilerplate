# npm-scripts-boilerplate
Simple JS project setup using NPM as a task runner

## Getting started
![](https://camo.githubusercontent.com/e9762d07d388e43fb4fcd7f4f525893afaefafad/68747470733a2f2f646c2e64726f70626f7875736572636f6e74656e742e636f6d2f752f313431323130302f6573362e6a7067)

### Yarn: Your new favourite package manager

- You'll need to have [Yarn](https://yarnpkg.com/en/docs/install) installed globally on your local machine. This can be installed via [homebrew](http://brew.sh/)
- To install all the dependencies for this project you will need to `yarn install` on the command line
- To add a dependency `yarn add {dependency}` on the command line.
- If it's a development dependency add the flag `--dev`. Example `yarn add {dependency} --dev` to save to the `package.json`
- If it's a production dependency add the flag `--save`. Example `yarn add {dependency} --save` to save to the `package.json`

### Task running
No time for bells and whistles, we're using good old NPM. It's best to have the node server and watcher/builder running at the same time, so you will need two terminals for this.

#### Node server
We are using `lite-server` as our node server to serve our web app, opens it in the browser, refreshes when html or javascript change.

_Command:_ `yarn run dev`

#### Watching and Building
Using `watchify` we are watching the `src` directory for changes and transpiling the ECMAScript 6 code to back down to ECMAScript 5, so that the browser can understand. The transpiled bundle is then moved to the `public/js` directory

_Command:_ `yarn run watch:bundle`

#### Deployment
We can deploy straight onto our `gh-pages` branch by running the command `yarn run gh-pages`. This will deploy the `public` directory to the `gh-pages` branch.

_Command:_ `yarn run gh-pages`
