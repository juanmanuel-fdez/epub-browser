epub-browser
============
epub-browser is a utility to browse and upload epub files on your file system using your browser. Its equivalent of creating a file share that can be accessed over http. Using this you can share files between different machines, and across different operating systems. 

Based on the [juanmanuel-fdez/file-browser](https://github.com/epub-browser/master/epub-browser) (and forked from [sumitchawla/epub-browser](https://github.com/sumitchawla/epub-browser)), this version offers a UI similar to pinterest showing the cover of the epub files. The covers of the files are created dynamically the fisrt time the system shows a file (using [krocon/node-ebook-cover-generator](https://github.com/krocon/node-ebook-cover-generator)). 

## How to install

The epub-browser uses the [node-ebook-cover-generator](https://github.com/krocon/node-ebook-cover-generator). This module has two main dependencies:

* [unpack-all](https://www.npmjs.com/package/unpack-all) to unpack the epub files and get the covers. Please, review the installation requirements of this module. 
* [GM](https://www.npmjs.com/package/gm) to process the images. If you only want to extract the covers without resizing it's not necessary any extra action.

```js
  npm install epub-browser
```

## How to Run
Change directory to the directory you want to browse. Then run the following command in that directory.
```js
  npm epub-browser
```
You would see the message <b>Please open the link in your browser http://<YOUR-IP>:8088</b> in your console. Now you can point your browser to your IP. 
For localhost access the files over http://127.0.0.1:8088 

epub-browser supports following command line switches for additional functionality.

```js
    -p, --port <port>        Port to run the epub-browser. Default value is 8088
    -e, --exclude <exclude>  File extensions to exclude. To exclude multiple extension pass -e multiple times. e.g. ( -e .js -e .cs -e .swp)
    -d, --directory <dir>    Path to the directory you want to serve. Default is current directory.
    -c, --cover              Create thumbnails from epub files. Default is false

``` 

## Screenshot
![alt File browser screenshot](https://raw.githubusercontent.com/juanmanuel-fdez/epub-browser/master/epub-browser.png)

## References & sources

### Original file-browser code
juanmanuel-fdez: [Code](https://github.com/epub-browser/master/epub-browser)

sumitchawla: [Blog post](https://chawlasumit.wordpress.com/2014/08/04/how-to-create-a-web-based-epub-browser-using-nodejs-express-and-jquery-datatables/) & [Code](https://github.com/sumitchawla/epub-browser)

### Upload feature 
FadyMak @ coligo-io [Blog post](https://coligo.io/building-ajax-file-uploader-with-node/) & [Code](https://github.com/coligo-io/file-uploader)

### Cover generator

krocon: [NPM] (https://www.npmjs.com/package/ebook-cover-generator) & [Code](https://github.com/krocon/node-ebook-cover-generator)

### Icons
[hawcons](https://www.iconfinder.com/iconsets/hawcons) by Yannick Lung

### Generic Logo
[gtdesigns](http://www.gtdesigns.it/overusedlogos/)
