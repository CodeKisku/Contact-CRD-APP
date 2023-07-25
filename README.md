# Svelte CRD APP
This is a simple CRUD (Create, Read, Delete) application built with Svelte JS. It allows you to create, edit and delete a contact with a name and an email field.

## How to use

You can clone this repository or download it as a zip file. Then, run the following commands in your terminal:

```bash
cd svelte-app
npm install
npm run dev
```

This will start a local server on port 5000. You can then open http://localhost:5000 in your browser. You can also view the live demo of the app by clicking [here](https://contact-svelte.netlify.app/).

## Features

- Svelte components
- Reactive variables and statements
- Event handling and binding
- Local storage

## Use Cases

- Add new contact with a name and an email
- Delete contact
- Store contact details in local storage

## Technologies

- Svelte JS: A modern JavaScript compiler that allows you to write easy-to-understand JavaScript code that is then compiled to highly efficient code that runs in the browser.

## Installation

To run this project locally, you need to have Node.js and npm installed on your machine. Then follow these steps:

1. Clone this repository: `git clone https://github.com/CodeKisku/Svelte-CRD-APP.git`
2. Navigate to the project directory: `cd Svelte-CRD-APP`
3. Install the dependencies: `npm install`
4. Start the development server: `npm run dev`
5. Open your browser and go to http://localhost:5000

## References

- [Building A CRUD Application with Svelte](https://codesource.io/building-a-crud-application-with-svelte/)
- [Simple CRUD app with Svelte JS](https://dev.to/miteshkamat27/simple-crud-app-with-svelte-js-k3g)

-----------------------------------------------------------------------------------------------------------
# svelte app

*Note that you will need to have [Node.js](https://nodejs.org) installed.*


## Get started

Install the dependencies...

```bash
cd svelte-app
npm install
```

...then start [Rollup](https://rollupjs.org):

```bash
npm run dev
```

Navigate to [localhost:8080](http://localhost:8080). You should see your app running. Edit a component file in `src`, save it, and reload the page to see your changes.

By default, the server will only respond to requests from localhost. To allow connections from other computers, edit the `sirv` commands in package.json to include the option `--host 0.0.0.0`.

If you're using [Visual Studio Code](https://code.visualstudio.com/) we recommend installing the official extension [Svelte for VS Code](https://marketplace.visualstudio.com/items?itemName=svelte.svelte-vscode). If you are using other editors you may need to install a plugin in order to get syntax highlighting and intellisense.

## Building and running in production mode

To create an optimised version of the app:

```bash
npm run build
```

You can run the newly built app with `npm run start`. This uses [sirv](https://github.com/lukeed/sirv), which is included in your package.json's `dependencies` so that the app will work when you deploy to platforms like [Heroku](https://heroku.com).


## Single-page app mode

By default, sirv will only respond to requests that match files in `public`. This is to maximise compatibility with static fileservers, allowing you to deploy your app anywhere.

If you're building a single-page app (SPA) with multiple routes, sirv needs to be able to respond to requests for *any* path. You can make it so by editing the `"start"` command in package.json:

```js
"start": "sirv public --single"
```

## Using TypeScript

This template comes with a script to set up a TypeScript development environment, you can run it immediately after cloning the template with:

```bash
node scripts/setupTypeScript.js
```

Or remove the script via:

```bash
rm scripts/setupTypeScript.js
```

If you want to use `baseUrl` or `path` aliases within your `tsconfig`, you need to set up `@rollup/plugin-alias` to tell Rollup to resolve the aliases. For more info, see [this StackOverflow question](https://stackoverflow.com/questions/63427935/setup-tsconfig-path-in-svelte).

## Deploying to the web

### With [Vercel](https://vercel.com)

Install `vercel` if you haven't already:

```bash
npm install -g vercel
```

Then, from within your project folder:

```bash
cd public
vercel deploy --name my-project
```

### With [surge](https://surge.sh/)

Install `surge` if you haven't already:

```bash
npm install -g surge
```

Then, from within your project folder:

```bash
npm run build
surge public my-project.surge.sh
```
