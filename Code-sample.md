[Wiki](Demos)> [Screenshots]> [Browser/device support]> [Options]> [Installing]> [How to use]> ** **

## Example code

The following code enables to select an image using a file input and crop it. The cropped image data is inserted into img each time the crop area updates.

```html
<html>
<head>
  <script src="angular.js"></script>
  <script src="ng-img-crop.js"></script>
  <link rel="stylesheet" type="text/css" href="ng-img-crop.css">
  <style>
    .cropArea {
      background: #E4E4E4;
      overflow: hidden;
      width:500px;
      height:350px;
    }
  </style>
  <script>
    angular.module('app', ['ngImgCrop'])
      .controller('Ctrl', function($scope) {
        $scope.myImage='';
        $scope.myCroppedImage='';

        var handleFileSelect=function(evt) {
          var file=evt.currentTarget.files[0];
          var reader = new FileReader();
          reader.onload = function (evt) {
            $scope.$apply(function($scope){
              $scope.myImage=evt.target.result;
            });
          };
          reader.readAsDataURL(file);
        };
        angular.element(document.querySelector('#fileInput')).on('change',handleFileSelect);
      });
  </script>
</head>
<body ng-app="app" ng-controller="Ctrl">
  <div>Select an image file: <input type="file" id="fileInput" /></div>
  <div class="cropArea">
    <img-crop image="myImage" result-image="myCroppedImage"></img-crop>
  </div>
  <div>Cropped Image:</div>
  <div><img ng-src="{{myCroppedImage}}" /></div>
</body>
</html>
```
