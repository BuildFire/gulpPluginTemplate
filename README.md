# gulpPluginTemplate - Alpha
simple template for a buildfire plugin to be bundled using gulp

run `npm install` to initialize the folder

then when ready for final test and release run `npm start` or `gulp build`
This will prodice a sister folder with `_release` as a postfix on teh root folder
thest his optomized copy then zip and publish


Note: If you are importing into an existing plugin project. Make sure you copy the `package.json` and `gulpfile.js` then when adding

- to combine your JS files simply surround them with this html comment:
`<!-- build:bundleJSFiles  -->...<!-- endbuild -->`
this will merge, minify and obfescate all files within these two comments into one JS file

example:
````
<!-- build:bundleJSFiles  -->
	<script src="app.js"></script>
	<script src="enums.js"></script>
	<script src="app.services.js"></script>
	<script src="controllers/content.home.controller.js"></script>
<!-- endbuild -->
````

In the release version this will be swapped out to reference a single file

- to combine your CSS files simply surround them with this html comment:
`<!-- build:bundleCSSFiles  -->...<!-- endbuild -->`
this will merge, minify and obfescate all files within these two comments into one CSS file

example:
````
    <!-- build:bundleCSSFiles  -->
    <link rel="stylesheet" type="text/css" href="css/a.css">
    <link rel="stylesheet" type="text/css" href="css/b.css">
    <!-- endbuild -->

````
