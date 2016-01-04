This project is a KML parser for use with Google Maps Javascript API Version 3.

This API is specifically designed to be about the creation of collapsible tree based layer control.



**Original code inspired by:**
  * Lance Dyas 	geoxml 	  project at:	http://code.google.com/p/geoxml/
  * Sterling Udell	geoxml3   project at: 	http://code.google.com/p/geoxml3/



**History:**



**General Notes:**
The focus is all about the displaying the contents in the side bar!
As a result there are many different configuration options.

_Support includes:_  polylines, polygons, markers, customizeable icons, and multiple kml files. KML Multi-Geometries are supported with an option to have simple circles for points instead of markers.

The optional dragzoom button on the map requires
`keydragzoom.js` or `keydragzoom_packed.js`
see  http://google-maps-utility-library-v3.googlecode.com



**Warnings:**  This Api does not contain any support of Google Maps Version 2.
Also the larger number of placemarks and shapes will result in slower loading!
Currently only a single Bubble is repeatedly used and there are no plans for multiple bubbles.

`KmlMapParser` is subject to the same cross-domain download restrictions as any Javascript, so any KML document you expect it to process will need to be served from the same domain as the containing map page.


**Examples :**

1. Download the `kmlExamples.zip` from the Downloads tab above.

2. Copy and then unzip it in your favorite server (Tomcat, Jboss, ...).

3. Open up a browser and bring up the kmlExamples default html page  ( http://localhost/kmlExamples/ )

4. This default page contains links to different examples and also an API.



**Basic Usage:**

1. Download `KmlMapParser.js` to your web site from the Source tab above.
> You may also need `keydragzoom.js` (see above).

2. Include it in your map page:

`<script src="KmlMapParser.js"></script>`

3. Instantiate and initialize the object, something like this:

```
var xml = new KmlMapParser({ map: map,
	   		   kml: '/path/to/data.kml',
     			   });
```



**For working examples, see the Downloads tab above for a zip file.**

**For more information, see the Wiki tab above.**