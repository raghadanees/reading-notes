## What Is Node.js?

#### Node.js® is a JavaScript runtime built on Chrome’s V8 JavaScript engine.

- it is an event-based, non-blocking, asynchronous I/O runtime that uses Google’s V8 JavaScript engine and libuv library.

The V8 engine is the open-source JavaScript engine that runs in Google Chrome and other Chromium-based web browsers, including Brave, Opera, and Vivaldi. It was designed with performance in mind and is responsible for compiling JavaScript directly to native machine code that your computer can execute.

 the creator of Node (Ryan Dahl) took the V8 engine and enhanced it with various features, such as a file system API, an HTTP library, and a number of operating system–related utility methods.

### This means that Node.js is a program we can use to execute JavaScript on our computers. In other words, it’s a JavaScript runtime.

### Node Binaries vs Version Manager
Many websites will recommend that you head to the official Node download page and grab the Node binaries for your system. While that works, I would suggest that you use a version manager instead. This is a program that allows you to install multiple versions of Node and switch between them at will. There are various advantages to using a version manager. For example, it negates potential permission issues when using Node with npm and lets you set a Node version on a per-project basis.

If you fancy going the version manager route, please consult our quick tip: Install Multiple Versions of Node.js using nvm. Otherwise, grab the correct binaries for your system from the link above and install those.

- You can check that Node is installed on your system by opening a terminal and typing node -v. If all has gone well, you should see something like v12.14.1 displayed.

### Node.js Has Excellent Support for Modern JavaScript

As can be seen on this compatibility table, Node has excellent support for ECMAScript 2015 (ES6) and beyond. As you’re only targeting one runtime (a specific version of the V8 engine), this means that you can write your JavaScript using the latest and most modern syntax. It also means that you don’t generally have to worry about compatibility issues — as you would if you were writing JavaScript that would run in different browsers.

To illustrate the point, here’s a second program that makes use of several modern JavaScript features, such as tagged template literals, object destructuring and Array.prototype.flatMap():

`function upcase(strings, ...values) {`

 ` return values.map(name => name[0].toUpperCase() + name.``slice(1))` `.join(' ') + strings[2];`

`}`

`const person = {`

 ` first: 'brendan',`

 ` last: 'eich',`

  `age: 56,`

 ` position: 'CEO of Brave Software',`

`};`


`const { first, last } = person;`

`const emoticon = [ ['┌', '('], ['˘', '⌣'], ['˘', ')', 'ʃ'] ];`


`console.log(`

  upcase`${first} ${last} is the creator of JavaScript! ` + emoticon.flat().join('')

`);`

Save this code to a file called index.js and run it from your terminal using the command node index.js. You should see Brendan Eich is the creator of JavaScript! ┌(˘⌣˘)ʃ output to the terminal.


## What Is Node.js Used For?

Now that we know what Node and npm are and how to install them, we can turn our attention to the first of their common uses: installing (via npm) and running (via Node) various build tools — designed to automate the process of developing a modern JavaScript application.

These build tools come in all shapes and sizes, and you won’t get far in a modern JavaScript landscape without bumping into them. They can be used for anything from bundling your JavaScript files and dependencies into static assets, to running tests, or automatic code linting and style checking.

We have a wide range of articles covering build tooling on SitePoint. Here’s a short selection of my favorites:

A Beginner’s Guide to Webpack
Up and Running with ESLint — the Pluggable JavaScript Linter
An Introduction to Gulp.js
Unit Test Your JavaScript Using Mocha and Chai
And if you want to start developing apps with any modern JavaScript framework (for example, React or Angular), you’ll be expected to have a working knowledge of Node and npm (or maybe Yarn). This isn’t because you need a Node back end to run these frameworks. You don’t. Rather, it’s because these frameworks (and many, many related packages) are all available via npm and rely on Node to create a sensible development environment in which they can run.

If you’re interested in finding out what role Node plays in a modern JavaScript app, read The Anatomy of a Modern JavaScript Application.


https://www.sitepoint.com/an-introduction-to-node-js/