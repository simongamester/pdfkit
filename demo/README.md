# ReSPECT Form Demo

The following demo has been adapted from the PDFKit main repo.

This pulls in v2 on the ReSPECT form and overlays with the required fields, each positioned within the document.
All PDFKit code can be found within browser.js, however this has been packaged in by Browserify and compiled into bundle.js.

## browser.js

This file contains a wrapper so it can be previewed within an html page (browser.html), however the code can be extracted from between `// START DOCUMENT` and `// END DOCUMENT`

The only exception to this is the use of images, which have been base64 encoded and included at the bottom of the file. A known constraint of Browserify is that is isn't able to utilise PDFKit's `fs.readFileSync`, however these should be included as separate assets elsewhere. I've located the page1 and page2 images within the /images folder for reference.

Assuming no further changes are made to the ReSPECT form, the content for the form has been abstracted into the a variable called 'form' which can be found at the top of the file. You should only need to change these values when generating the form. The sliders as integers between 1 and 100 and position themselves correctly on the form as an 'X'. Tick boxes are a series of boolean values, so just set them to true / false to determine which boxes to check.

## Installation

`npm install`
`npm run build`
`npm run browser-demo`

## Development

It's possible to view live updates of the browser.js by using watchify:

`cd demo`
`watchify browser.js -o bundle.js -v`
