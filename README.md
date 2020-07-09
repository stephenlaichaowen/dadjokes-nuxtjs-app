# Project : DadJokes

## Demo website is [here](https://dadjokes-nuxtjs-app.netlify.app/)

This project is built with Nuxtjs, the most powerful and advanced fullstack framework ever that empowers your single page application with server side render functionality and more ...

This project access remote api (jokes) to read the joke lists and prepopulate in server then render in browser. If you click right in mouse panel and select `inspect page source code` you will see the contents. This is vue-cli can't offer and that makes nuxtjs stands out !!!

## This is a small, simple but practical project that involves the following tech:

- In asyncData hooks using axios to retrieve remote api [dadjokes api](https://icanhazdadjoke.com) to get data, and prepopulate the static content in server side before page render
- Page transition is applied: configure nuxt.config.js and register transtion property, add global css code

## How to build this project

```bash
# first download this project to your desktop

# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# generate static project
$ npm run generate
```

## Things to know when deploying project to Netflify

There is one thing you should pay attetion to when deploying Nuxutjs project in Netlify, in step 3 ~ Build options, and deploy!, you have to fill out `Build command` and `Publish directory` like

```
Build commnad : npm run generate
Publsih directory : dist
```

Then Netlify will build the project for you automatically and deploy !!!

This project is inspired by [Nuxt JS Crash Course / Traversy Media](https://www.youtube.com/watch?v=ltzlhAxJr74), the author didn't apply ssr to the project and I enhance it with ssr functionality.

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).
