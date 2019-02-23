# Ionic 4 with Vue

> An Ionic + Vue.js project

## Config Vue

``` bash
# install vue
npm install vue-cli -g

# create project vuejs
vue init webpack-simple i-vue

# install dependencies
cd i-vue
npm install

# serve with hot reload at localhost:8080
npm run dev
```

## Config Ionic4

set in index.html

``` html
<meta name="viewport" content="width=device-width,initial-scale=1.0">

<link href="https://unpkg.com/@ionic/core@4.0.2/css/ionic.bundle.css" rel="stylesheet">
<script src="https://unpkg.com/@ionic/core@4.0.2/dist/ionic.js"></script>
```

## Build and run device  with Capacitor

``` bash
npm install --save @capacitor/core @capacitor/cli

npx cap init ionic-vue ga.hhalmeida.ionicvue
```

 - Change webpack config to build files in 'www' folder 

 ``` js
 build: {
    // Template for index.htmlc
    index: path.resolve(__dirname, '../www/index.html'),
 
    // Paths
    assetsRoot: path.resolve(__dirname, '../www'), 
    ...
  }
 ``` 

 - Android
    npx cap add android
    npx cap sync
    npm run build
    npx cap copy
    npx cap open android


 - iOS
 - if you don't instaled cocoapods 
 ``` bash
    gem install cocoapods
 ```

``` bash
    npx cap add ios
    npx cap sync
    npm run build
    npx cap copy
    npx cap open ios
```

## References

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

https://ionicframework.com/docs/

https://www.npmjs.com/package/@ionic/core

https://capacitor.ionicframework.com/docs/getting-started/

https://guides.cocoapods.org/using/getting-started.html#installation
