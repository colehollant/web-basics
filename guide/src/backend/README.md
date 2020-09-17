# Installation

To install the `feathers` CLI, we will need to add it globally:

```sh
yarn global add @feathersjs/cli
```

We will then make a directory for the backend and generate an app. I'll include some suggested values for the CLI tool.

```sh
mkdir backend && cd backend
feathers generate app
# App generation prompts & responses
? Do you want to use JavaScript or TypeScript? JavaScript
? Project name backend
? Description some little backend
? What folder should the source files live in? src
? Which package manager are you using (has to be installed globally)? Yarn
? What type of API are you making? REST
? Which testing framework do you prefer? Mocha + assert
? This app uses authentication Yes
? Which coding style do you want to use? ESLint
? What authentication strategies do you want to use? (See API docs for all 180+ supported oAuth providers) Username + Password (Local)
? What is the name of the user (entity) service? users
? What kind of service is it? Mongoose
? What is the database connection string? mongodb://localhost:27017/backend
```

That being said, I truly don't know much about Feathers specifically, but I'll mess with it soon and be more helpful! It seems like their [site is super well documented though](https://docs.feathersjs.com/guides/basics/setup.html#what-we-will-do).