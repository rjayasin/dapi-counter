# dapi-counter

An automated image analysis tool for counting DAPI-stained nuclei on the perimeter of organoids.

**[rjayasin.github.io/dapi-counter](https://rjayasin.github.io/dapi-counter/)**

Upload a DAPI image of one or more organoids (JPEG, PNG, TIFF or HEIC). The tool finds each nucleus, outlines each organoid, and counts the nuclei that lie on its perimeter, along with the perimeter length and the number of perimeter nuclei per 100 µm. Click nuclei to switch them between perimeter and interior, click to add ones it missed, or right-click to remove false detections, then download the counts as an xlsx.

Everything runs in the browser from a single `index.html` with no build step; images are never uploaded anywhere. HEIC images open natively in Safari; other browsers load a decoder ([heic2any](https://github.com/alexcorvi/heic2any)) from a CDN the first time one is opened. To run it locally, serve the folder with any static file server, e.g. `python3 -m http.server`.
