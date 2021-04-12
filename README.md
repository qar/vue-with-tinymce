# vue-with-tinymce

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

### Add Tinymce

1. Install editor core with vue component

```
npm install --save tinymce
npm install --save @tinymce/tinymce-vue@^3
```

`@tinymce/tinymce-vue` Version 4.0 is intended to support Vue 3. For Vue 2.x and below please use previous versions of the wrapper.

2. Copy skins assets

```
mkdir -p public/tinymce
cp -r node_modules/tinymce/skins public/tinymce
```
