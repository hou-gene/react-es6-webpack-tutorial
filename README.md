# React, Webpack, and ES6
This is a rewrite of the vanilla Facebook tutorial, but using (mostly) ES6:
https://facebook.github.io/react/docs/tutorial.html

## Node / npm
Node.js brought npm (node package manager) to the ecosystem. Think of this as a global repository for libraries. Dependencies are defined within a package.json in a project and upon execution of

`npm install`

in the directory of a package.json, git will clone repos of those dependencies down to your local machine. There is a pre-requisite that Git (https://git-scm.com) or GitHub (https://mac.github.com or https://windows.github.com) be installed.

## Webpack
Webpack is a build tool, same category as Gulp and Grunt (you can see some here: https://babeljs.io/docs/using-babel/. Docs on the official repo are hit and miss, but basically what webpack does is at least a few things (i'm sure more too).
#####Detects changes in targetted local files, emits a refresh to browser.
- Makes development cycle much better experience when you change a js file and the browser auto-reloads

#####Bundles your dependencies into a bundle file or many bundle files depending on how many entry points your SPA has.
- Instagram, for example has 17 entrypoints and each entrypoint is compiled at production buildtime to only include dependencies for that entrypoint. This way you don't need to load all libraries on the initial load for a SPA - improving over the wire performance. I think there are ways to configure so if multiple entrypoints share the same code, it's not refreshed over the wire when switchin between the two (cached in browser, and Webpack knows this).

#####Handles ES6 and JSX (react specific syntax) via Babel / Babel-loader
- Babel is a transpiler library, and you can tell Webpack to use them at build time to transpile ES6 to ES5, or convert the React specific JSX syntax over to regular javascript. 


#Installation
On windows: open node.js command prompt
on OSX: open terminal

`git clone https://github.com/hou-gene/react-es6-webpack-tutorial`

navigate to root

`npm install`

`npm start`

Notice that npm start is defined within package.json under scripts. This will start two servers. A backend node server, and our webpack dev server. Open the following url to view

`localhost:8090`