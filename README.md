# Project : DadJokes

## Demo website is [here](https://dadjokes-nuxtjs-app.netlify.app/)

This project is built with Nuxtjs, the most powerful and advanced fullstack framework ever that empowers your single page application with server side render functionality and more ...

This project access remote api (jokes) to read the joke lists and prepopulate in server then render in browser. If you click right in mouse panel and select `inspect page source code` you will see the contents. This is vue-cli can't offer and that makes nuxtjs stands out !!!

## This is a small, simple but practical project that involves the following tech:

- Using axios to retrieve remote api [dadjokes api](https://icanhazdadjoke.com) to get data
- The retrieved data then store using asyncData hooks, page then prepopulated in server side before page render
- Page transition is applied: configure nuxt.config.js and register transtion property, add global css code

## How to build this project

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# generate static project
$ npm run generate
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).
