[Wiki](Demos)> [Screenshots]> [Browser/device support]> **Options**

## Options

```html
<img-crop
    image="{string}"
    result-image="{string}"
    result-array-image="{array}"
    result-blob="{string}"
    url-blob="{string}"
    area-coords="myAreaCoords"
   [change-on-fly="{boolean}"]
   [init-max-area="true"]
   [allow-crop-resize-on-corners="true"]
   [live-view="{object}"]
   [area-type="{circle|square|rectangle}"]
   [area-min-size="{ number|{w:number,h:number} }"]
   [area-min-relative-size="{ number|{w:number,h:number} }"]
   [cropject="{cropWidth:number,cropHeight:number,cropTop:number,cropLeft:number}"]
   [area-init-size="{ number|{w:number,h:number} }"]
   [result-image-size="{ number|{w:number,h:number}|[{w:number,h:number},{w:number,h:number},...] }"]
   [result-image-format="{string}"]
   [result-image-quality="{number}"]
   [aspect-ratio="{number}"]
   [dominant-color="{string}"]
   [palette-color="{string}"]
   [palette-color-length="{number}"]
   [on-change="{expression}"]
   [on-load-begin="{expression"]
   [on-load-done="{expression"]
   [on-load-error="{expression"]
></img-crop>
```

### image

Assignable angular expression to data-bind to. NgImgCrop gets an image for cropping from it.

* Notice for mobile device:
Using Data URI is very slow on mobile device, 6x slower. (http://www.mobify.com/blog/data-uris-are-slow-on-mobile/)
Provide instead a blob.

### result-image

Assignable angular expression to data-bind to. NgImgCrop puts a data uri of a cropped image into it.

### result-blob

Assignable angular expression to data-bind to. NgImgCrop puts a blob of a cropped image into it.

### url-blob

Assignable angular expression to data-bind to. NgImgCrop puts an url blob of a cropped image into it.

### change-on-fly

*Optional*. By default, to reduce CPU usage, when a user drags/resizes the crop area, the result image is only updated after the user stops dragging/resizing. Set true to always update the result image as the user drags/resizes the crop area.

### live-view

*Optional*. By default, to reduce CPU usage and lag mostly for huge result images, when a user drags/resizes the crop area, the result image is only updated after the user stops dragging/resizing. This is a bit complex part then change on fly, to make it work you have to create object in your controller and assign a variable block to it with try value. After that cropper will bind function "render" which will accept callback and that callback will return dataURL. Example of object {block: true}.

### init-max-area

*Optional*. This initialize the crop area with max size, depends on the type and aspect ration.

### allow-crop-resize-on-corners

*Optional*. This allow to enable resize of the crop area when it come near corners.

### area-type

*Optional*. Type of the crop area. Possible values: circle|square|rectangle. Default: circle.

### area-min-size

*Optional*. Min. width/height of the crop area (in pixels). Default: 80.

### crobject

*Optional* Gives the opportunity to add an object to the cropper that gives information about the crop dimensions while croppping and selecting an image.

### area-min-relative-size

*Optional*. Min. width/height of the crop area (in pixels) relative to original image width/height. Usable if you use `result-image-size="'max'"` and want to get image larger that specified limit.

### area-init-size

*Optional*. Min. width/height of the crop area (in pixels) to start with, overriding the standard 200*200 crop area ratio. Default: false

### result-image-size

*Optional*. Width/height of the result image (in pixels). Default: 200.
'selection' renders an image of the size of the area selected.
'max' maximizes the rendered image.

### result-array-image

While you have added an array inside of option result-image-size you will have option to get array of dataURI alogside with width and height requested.

### result-image-format

*Optional*. Format of result image. Possible values include image/jpeg, image/png, and image/webp. Browser support varies. Default: image/png.

### result-image-quality

*Optional*. Quality of result image. Possible values between 0.0 and 1.0 inclusive. Default: browser default.

### aspect-ratio

*Optional*. For rectangle area type. Maintain aspect ratio by scale width/height number.

### dominant-color

*Optional*. Provide dominant color for image using color-thief (https://github.com/lokesh/color-thief).

### palette-color

*Optional*. Provide a color palette for image using color-thief (https://github.com/lokesh/color-thief).

### palette-color-length

*Optional*. Provide a color palette for image using color-thief (https://github.com/lokesh/color-thief).

### on-change

*Optional*. Expression to evaluate upon changing the cropped part of the image. The cropped image data is available as $dataURI.

### on-load-begin

*Optional*. Expression to evaluate when the source image starts loading.

### on-load-done

*Optional*. Expression to evaluate when the source image successfully loaded.

### on-load-error

*Optional*. Expression to evaluate when the source image didn't load.

### chargement

*Optional*. Allow you to modify text of loading message.
