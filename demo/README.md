# ReSPECT Form Demo

The following demo has been adapted from the PDFKit main repo.

This pulls in v2 on the ReSPECT form and overlays with the required fields, each positioned within the document.
All PDFKit code can be found within browser.js, however this has been packaged in by Browserify and compiled into bundle.js.

## browser.js

This file contains a wrapper so it can be previewed within an html page (browser.html), however the code can be extracted from between `// START DOCUMENT` and `// END DOCUMENT`

The only exception to this is the use of images, which have been base64 encoded and included at the bottom of the file. A known constraint of Browserify is that is isn't able to utilise PDFKit's `fs.readFileSync`, however these should be included as separate assets elsewhere. I've located the page1 and page2 images within the /images folder for reference.
