# Installation

You will need to have `node` installed (and out of my own stubborness I will tell you to install `yarn`, but feel free to use `npm` instead).

If you don't have these already (I don't remember if macOS started having it by default...), you can just install with homebrew:

```sh
brew install node
brew install yarn
```

If you want to toy around with standard Vue (without Nuxt), you can use it through a CDN (as was in the previous example) or through their CLI tool:

```sh
npm install -g @vue/cli
# OR
yarn global add @vue/cli
```

Otherwise, to create a Nuxt app... we can use `yarn create`:

```sh
yarn create nuxt-app <name of project>
```

This will spin up a little CLI tool that bootstraps your project, the following are a nice set of options to get started:

```sh
create-nuxt-app v3.2.0
✨  Generating Nuxt.js project in <name of project>
? Project name: <name of project>
? Programming language: JavaScript
? Package manager: Yarn
? UI framework: Tailwind CSS
? Nuxt.js modules: Axios, Progressive Web App (PWA), Content
? Linting tools: 
? Testing framework: None
? Rendering mode: Universal (SSR / SSG)
? Deployment target: Static (Static/JAMStack hosting)
? Development tools: jsconfig.json (Recommended for VS Code if you're not using typescript)
```

Then, as it says, we launch the development server with:

```
cd <name of project>
yarn dev
```