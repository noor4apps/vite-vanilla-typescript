# Creating a JavaScript library

## Create a new project

λ npm init vite@latest
√ Project name: ... vite-vanilla-typescript
√ Select a framework: » Vanilla
√ Select a variant: » TypeScript


## Remove obsolete files
Remove the following files as they are not needed in a NPM package:
• favicon.svg
• typescript.svg
• app.css (or style.css)
• index.html
• main.ts
• counter.ts
Remove also the public directory and all its contents.

## Add main entry index.ts file
Add new new file under src/ called index.ts that export all the source code we want to exposes from our NPM package. 
In our case, we’ll export everything from the sub-directory called helpers

## Update or create vite.config.ts
## Update package.json commands
add additional configuration so that the project will build as a library

## Add a some JavaScript helpers to our NPM package
## Unit tests

Before we try to run our tests, let’s install vitest and additional unit-test dependencies we need with

```shell
npm install -D vitest @types/jest jsdom
```

and then add the following 2 new commands to the package.json scripts section

## Build the library

To build the library, just run the command 

```shell
npm run all
```

(not this will also pack the library into a compressed file with .tgz extension and we could later consume from there or just by referencing the local directory)

## Consuming the vite-vanilla-typescript library
Now we have to open the vite-vue-project and consume our helpers library by referencing it from a local path. 
The easiest way is to run the following command

```shell
npm install -D file:../vite-vanilla-typescript
```
Note that we are referencing our helpers library with a relative directory path so it is important that you have create the vite-vanilla-typescript project at the same level of vite-vue-project.
To test that we can consume our library without problems, open one of the views, maybe App.vue, and import a reference to randomid And then output the value in the UI with some HTML like:
<p>[randomid() result (from vite-vanilla-typescript): {{ randomid() }}]</p>
