# example-4d-vue.js

Example of 4d database to serve builded [Vue.js](https://vuejs.org/) website.

## What is vue.js?

Vue.js is a JavaScript Framework to build website.

A vue is a combinaison of html template, javascript code and css. (ex: https://vuejs.org/images/vue-component.png)

- Documentation: https://vuejs.org/v2/guide/
- [Vue.js Explained in 100 Seconds](https://www.youtube.com/watch?v=nhBVL41-_Cw)

## Create a Vue.js website

First install vue-cli: https://cli.vuejs.org/guide/installation.html

Then [create a vue project](https://cli.vuejs.org/guide/creating-a-project.html#vue-create), for instance with "vue" name

```bash
vue create vue 
```

A [vue](vue) folder will be created with all needed files: vues, node packages and a readme.

### Use an web insterface to create project and configure

```bash
vue ui 
```

It is a really good alternative because it will help you to configure and to add additionnal tools and package such as `vue-rooter`

#### Rooter

Rooter allow to execute code or display page according to the URL.

You can see change introduced by installing the [`vue-rooter`]( https://router.vuejs.org/) in this [pull request](https://github.com/mesopelagique/example-4d-vue.js/pull/1/files)

### How to download node packages for this repository?

This repository contains already a [vue project](vue). If you use it and just downloaded it, you must install javascript package using npm command

```bash
cd vue
npm install
```

A node_modules folder will be created

## Build the website

Go to your vue project folder and launch build

```bash
cd vue
npm run build
```

### How to build a vue.js website to a specific folder?

4D server use [WebFolder](WebFolder) directory as main web server directory, so when building your Vue.js website you must configure the output directory.

So you must create or edit the [vue.config.js](vue/vue.config.js) inside your website project to specify the "WebFolder" as [output directory](https://cli.vuejs.org/config/#outputdir). (It's already done for this project)

Then any `npm build` will remove your WebFolder and replace it with the new builded website.

PS: alternatively, you can add extra step to copy builded files. The default path is `dist`

## How to develop with vue.js

### IDE

You could use [Visual Studio Code](https://code.visualstudio.com/) with [vue.js expansion pack](https://marketplace.visualstudio.com/items?itemName=mubaidr.vuejs-extension-pack)

### Preview change

Launch a webserver to preview a "development build" with auto-reload ie. each time you edit a file, the modifications are applied immediately

```bash
cd vue
npm run serve
```

### Debugging

You can install browser extension. 

For chrome [the extension is available here](https://chrome.google.com/webstore/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd?hl=fr).

## Exchanging data between front-end (vuejs) and backend (4d)

4D backend using `on web connection` or using 4Daction could provide endpoint to provide data, as text, json, images, etc...

The vue.js frontend will request this data using your favorite http request node package ([http, https, asio, etc...](https://www.twilio.com/blog/2017/08/http-requests-in-node-js.html)) and fill the template.

A simple example is provided by this [pull request](https://github.com/mesopelagique/example-4d-vue.js/pull/2/files)
