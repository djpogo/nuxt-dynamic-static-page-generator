# nuxt dynamic static page generator

This is the demo project of [this blog post](https://raoulkramer.de/nuxt-js-static-page-generator-with-dynamic-pages/).

The project will read 20 items of the dog api and create an index page and 20 detail pages too, by consuming the api.

During `npm run generate` the dog api is read and added as [`routes`](https://github.com/djpogo/nuxt-dynamic-static-page-generator/blob/main/nuxt.config.js#L65). Nuxt will build all dog api content as static pages then.

For a real world app you can call `npm run generate` everytime your api endpoint changes and your website will renew itself.

## setup

``` bash
$ npm install
$ npm run generate
$ ls -l ./dist
```
