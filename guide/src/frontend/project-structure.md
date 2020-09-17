# Project Structure

Out of the box, Nuxt gives us _a lot_. We may not need all of this, but let's give a quick walkthrough regardless.

For my sake, I will assume your `<name of project>` is `frontend` here, in case you wonder where that comes from. Within the `frontend` directory that it creates, we see a whole bunch of subdirectories and files:

- **`/.nuxt/`** gets generated / updated each time you spin up the dev server, don't worry about this
- **`/assets/`** folder for assets! things like images, css, fonts, etc
- **`/components/`** folder for Vue components that aren't directly rendered by routes
- **`/content/`** (only if you added @nuxt/content) folder for your markdown files
- **`/layouts/`** folder for component layouts, you likely don't need to worry about this yet, but if you have one layout with a header and a footer that gets used for several pages and one without, that's the point!
- **`/middleware/`** folder for component middleware, you likely don't need to worry about this yet, essentially can make little functions that get called before rendering a page
- **`/node_modules/`** just where all your dependecies are stored, do not edit (unless you delete the whole folder and reinstall via `yarn install`)
- **`/pages/`** folder with components rendered by current route!
- **`/plugins/`** folder with js / vue plugins, if you need to register directives or use polyfills, here's where ya do it
- **`/static/`** folder with statically served files!
- **`/store/`** folder with Vuex stores, if you need more sophisticated state management, could be worth looking into!
- **`/.editorconfig`** literally who cares
- **`/.gitignore`** files that dont get source controlled
- **`/jsconfig.json`** couldn't tell ya... might be how some of the webpack stuff with `~/` gets set up?
- **`/nuxt.config.js`** your nuxt configuration! edit as you need 
- **`/package.json`** list of dependencies / versions, as well as scripts 
- **`/README.md`** lol who care
- **`/tailwind.config.js`** tailwind config, feel free to extend as you need
- **`/yarn.lock`** just current state of packages

The things you will probably care the most about are `/pages`, `/components`, `/nuxt.config.js` and maybe `/assets`, the rest sorta pop up as you need them (`/store` might be a big one if you need it!).

The `/pages` directory _does_ determine your routing (you can override if necessary), based off of the file structure. If you have `/pages/about.vue` there will be a route for `/pages/about` that points to the component defined in `/pages/about.vue`, and it can be as nested as you need! I'd recommend [looking at their docs](https://nuxtjs.org/guide/routing) if you need some dynamic routing though.