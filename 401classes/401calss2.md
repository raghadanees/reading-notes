# Classes, Inheritance, Functional Programming

Test-driven development (TDD) is a technique for ensuring that your code does what you think it does. It’s particularly relevant for JavaScript, with its cross-browser incompatibilities and hidden gotchas. With TDD, you express your intentions twice: once as a test, and once as production code. If the two approaches don’t match, your tests fail, and you’ve caught a bug.

TDD is a great way of catching the majority of programming errors. It’s not perfect, of course—in particular, it can’t tell you when your assumptions are wrong—but it’s very good at catching the kinds of bugs JavaScript is prone to.

## Inheritance and the prototype chain.

*When it comes to inheritance, JavaScript only has one construct: objects. Each object has a private property which holds a link to another object called its prototype. That prototype object has a prototype of its own, and so on until an object is reached with null as its prototype. By definition, null has no prototype, and acts as the final link in this prototype chain.*

Nearly all objects in JavaScript are instances of Object which sits on the top of a prototype chain.

*While this confusion is often considered to be one of JavaScript's weaknesses, the prototypal inheritance model itself is, in fact, more powerful than the classic model. It is, for example, fairly trivial to build a classic model on top of a prototypal model.*

### this
A property of an execution context (global, function or eval) that, in non–strict mode, is always a reference to an object and in strict mode can be any value.

In the global execution context (outside of any function), this refers to the global object whether in strict mode or not.

### classes

Classes are a template for creating objects. They encapsulate data with code to work on that data. Classes in JS are built on prototypes but also have some syntax and semantics that are not shared with ES5 classalike semantics.

![Image](https://miro.medium.com/max/441/0*Xms6_7ml3f1DAP93.png)

Terms
Ecosystem The JavaScript ecosystem is a collection of software packages, libraries, and other resources that facilitate development as they integrate with each other.

Node.js® is a JavaScript runtime built on Chrome’s V8 JavaScript engine.

V8 JavaScript engine is Google’s open source high-performance JavaScript and WebAssembly engine, written in C++. It is used in Chrome and in Node. js, among others.

module A module is just a file. One script is one module. As simple as that.modules can load each other and use special directives export and import to interchange functionality,

A package is one or more modules (libraries) grouped (or packaged) together.

node package manager is a command line tool that installs, updates or uninstalls Node. js packages in your application. It is also an online repository for open-source Node. js packages.

Server is an extended version of JavaScript that enables back-end access to databases, file systems, and servers.

environment gives you support for file access, network access, database access etc.

Interpreter is a program that executes instructions written in a high-level language.

A compiler is a program that translates code written in a high-level programming language into low-level code directly executable by the computer or another program such as a virtual machine.


- Why would you want to run JavaScript code outside of a browser? 

Running JavaScript inside a browser means you are interacting with Web UI (HTML and CSS components) which is displayed on a user’s screen. Running JavaScript without/outside a browser means you are using node. js technology to execute your JavaScript code.

- What is the difference between a module and a package?

A module is a file (or files) that are imported under one import and used. e.g. A package is a collection of modules in directories that give a package hierarchy.

- What does the node package manager do? 
Node Package Manager (NPM) is a command line tool that installs, updates or uninstalls Node. js packages in your application. It is also an online repository for open-source Node.

- Provide code snippets showing 3 different ways to export a function from a node module

exports.FucName = () => { return 'xxxx'; };
module.exports = FucName();
module.exports = 'xxxx';