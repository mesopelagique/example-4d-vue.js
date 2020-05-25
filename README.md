# example-4d-vue.js

Example of 4d database to serve builded [Vue.js](https://vuejs.org/) website.

## Create a Vue.js website

First install vue-cli: https://cli.vuejs.org/guide/installation.html

Then [create a vue project](https://cli.vuejs.org/guide/creating-a-project.html#vue-create), for instance with "vue" name

```bash
vue create vue 
```
or to use a web interface to configure the project
```bash
vue ui 
```

A [vue](vue) folder will be created with all needed files: vues, node packages and a readme.

### How to download node packages for this repository

This repository contains already a [vue](vue)  If you use it, you must install package using npm command

```bash
cd vue
npm install
```

## How to build a vue.js website to specific folder?

4D server use [WebFolder](WebFolder) directory as main web server directory, so when building your Vue.js website you must configure the output directory.

So you must create or edit the [vue.config.js](vue/vue.config.js) inside your website project to specify the "WebFolder".

Then `npm build` will remove your the WebFolder and replace with new builded website.

PS: alternatively, you can add extrat step to copy builded files, default path is `dist`
