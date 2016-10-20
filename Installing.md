[Wiki](Demos)> [Screenshots]> [Browser/device support]> [Options]> **Installing**

## Installing

### Download

You have four options to get the files:
- [Download ngImgCropExtended](https://github.com/CrackerakiUA/ngImgCropExtended/archive/master.zip) files from GitHub.
- Use Bower to download the files. Just run `bower install ngImgCropFullExtended`.
- Use Npm to download the files. Just run `npm i ng-img-crop-full-extended`.
- Use Meteor to download the files. Just run `meteor add correpw:ng-img-crop-full-extended`.

### Add files

Add the scripts to your application. Make sure the `ng-img-crop.js` file is inserted **after** the `angular.js` library:

```html
<script src="angular.js"></script>
<script src="ng-img-crop.js"></script>
<link rel="stylesheet" type="text/css" href="ng-img-crop.css">
```

### Add a dependancy

Add the image crop module as a dependancy to your application module:

```js
var myAppModule = angular.module('MyApp', ['ngImgCrop']);
```
