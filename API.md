# `KmlMapParser` API #

`KmlMapParser` makes it easy to control the look of the sidebar and its contents. Below are the configuration options - case matters!

| **Config Option Name** | **param** | **description** |
|:-----------------------|:----------|:----------------|
| afterParseFn           | Object    | A Javascript function to be called after parsing the KML files.|
| allFoldersOpen         | Boolean   | If this is defined it will override ALL the KML folder open tags so that the tree will always be closed or opened; default is undefined and will honor KML folder open tags.|
| dragZoomButtonImage    |String	    | The image file to use for the dragZoomButton. example: '![http://localhost/kmlExamples/resources/images/dragzoom_btn.png](http://localhost/kmlExamples/resources/images/dragzoom_btn.png)'. The default is '![http://maps.gstatic.com/mapfiles/ftr/controls/dragzoom_btn.png](http://maps.gstatic.com/mapfiles/ftr/controls/dragzoom_btn.png)';|
| highlightColor         | String    | An RGB color that all shapes will be highlighted to show a selected state. Default is a light bright blue - '#aaffff'.|
| imageDirectory         | String    | the directory location of the images, example: 'http://localhost/kmlExamples/resources/images'; default is to use the directory indicated in the KML stylesheet.|
| imageSize              | Object    | Specifies the width and height of ALL marker images. Using this will override the default size for marker images. example: {width: 16, height:18}; default for Google Maps uses a 32 x 32 image or {width: 32, height:32}. |
| imageHotspot           | Object    | It specifies the pixel position within the icon that is "anchored" to the point specified in the Marker. Using this will override the default anchor for ALL marker images it will NOT override a KML 'hotspot'. example: {x: 0, y:32}; Google Maps uses a 32 x 32 image as the default size so the default hotspot is the bottom middle of the image or {x: 16, y:32} |
| showImageShadow        | Boolean   | Tries to add a google marker shadow. If no KML styles are used a shadow is always shown. Default is false which will NOT display any marker shadows.|
| kml                    | String or Array | KML file to be parsed. Example '../kmlFiles/sidebarMap.kml', 'http://myServer.com/kmlFiles/state_capitals.kml'].    Note that the KmlMapParser is subject to the same cross-domain download restrictions as any JavaScript, so any KML document will need to be served from the same domain as the html map page.|
| map                    | Map Object |Google v3 map. REQUIRED |
| sidebarId              | String    | html id where the side bar will be created; the default id is 'the\_side\_bar' |
| showBubble             | Boolean   | true to show the bubble/balloon on the map; false to suppress it (and zoom and hilight); default is true.|
| showDragZoomButton     | Boolean   | true to show the dragzoom button on the map. [REQUIRES keydragzoom.js or keydragzoom\_packed.js.js see http://google-maps-utility-library-v3.googlecode.com|
| showFolders	           | Boolean   | true to show the side bar in a tree; false will display the contents in a unordered list; default is true.|
| showSidebar            | Boolean   | true to show the side bar;  false will not display the sidebar; default is true.|
| showOverlaysInSidebar  | Boolean   |true to show overlays in the side bar; false will not display any overlays in the sidebar; default is true.|
| showSidebarDescriptions | Boolean   | true to show descriptions in the side bar, false will not show descriptions; default is true.|
| showSidebarBubble      | Boolean   | true display a map bubble when clicking an item in the side bar; default is false.|
| showRootName           | Boolean   | true to display the document name as the root of the file contents when shown in the sidebar; default is true.|
| showMultiPointsAsMarkers | Boolean   | true to show the KML multigeometry points as a google map marker, false will show them as a circle; default is false;|
| sidebarId              | String    | html id where the side bar will be created; the default id is 'the\_side\_bar'.|
| useMapCenter           | Boolean   | true to use the google map lat/long center as the center of the map, false will use the actual KML to determine the bounds of the map; default is false; |
| zoomLevel              | Number    | a google maps zoom level that will be used to zoom the map when you click on the sidebar marker name; default zoomLevel is 15;|
| zoomOnClick            | Boolean   | true to zoom the map when you click on the sidebar marker name, false to remain at the current zoom; default is true;|

## Public Methods ##

**parse** _( String or Array urls )_
Process one or more KML documents.


**hideDocumentById** _( String docId )_
Show the map objects associated with a document by the documents id.


**showDocumentById** _( String docId )_
Show the map objects associated with a document by the documents id.


**setVisibility** _( Boolean isVisible )_
Sets visibility on all map objects and the sidebar.


**setVisibilityOnMarkers** _( Boolean isVisible, Number docId )_
Sets visibility on all map markers and shapes.


**setOverlayVisibility** _( Boolean isVisible )_
sets all the overlays to the specified opacity.


**setOverlayOpacity** _( Number opacity )_
sets the Overlay opacity (1-100) for all overlays on the map


**setOverlayOpacityByDocId** _( Number docId, Number opacity )_
sets the overlay opacity by the documents id.


**clearMap**
clears Map of all object displayed on it and removes contents the side bar and destroys all references to the KML there is no recovery from this action except to re-parse the KML.


**filterSidebar** _(String text)_
filters the Sidebar contents.


**filterMarkers** _(String text)_
filters Markers on all map markers and shapes by the description.


**filterMap**  _(String text)_
filters both the Sidebar and the markers on the map.


**zoomMap** _(Number zoomLevel)_
level to zoom the map


**closeBubble**
closes the bubble on the map.
