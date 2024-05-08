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