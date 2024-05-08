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