[Wiki](Demos)> [Screenshots]> [Browser/device support]> [Options]> [Installing]> **How to use**

## Usage

1. Add the image crop directive `<img-crop>` to the HTML file where you want to use an image crop control. *Note:* a container, you place the directive to, should have some pre-defined size (absolute or relative to its parent). That's required, because the image crop control fits the size of its container.
2. Bind the directive to a source image property (using **image=""** option). The directive will read the image data from that property and watch for updates. The property can be a url to an image, or a data uri.
3. Bind the directive to a result image property (using **result-image=""** option). On each update, the directive will put the content of the crop area to that property in the data uri format.
4. Set up the options that make sense to your application.
5. Done!