OpenFusion GeoJSON Visualizer
=============================

Vizit creates mobile-friendly visualizations for geotagged data using HTML5 and CSS3.
It retrieves GeoJSON files via AJAX and produces maps using Leaflet.js and OpenStreetMap.
See the [documentation](https://ogre.readthedocs.org/en/latest/about.html) of OGRe, a complemental project, for more on the history and architecture of vizit.

[![Screenshot](https://openfusion-dev.github.io/vizit/images/screenshot.png)](https://openfusion-dev.github.io/vizit/)

## Installation

To get Vizit, use one of the following methods:

1. [GitHub](https://github.com/openfusion-dev/vizit/archive/master.zip) (recommended)
2. git
```shell
$ git clone https://github.com/openfusion-dev/vizit.git
```

## Usage

To use Vizit, you must open `index.html` in your favorite browser.

### Note

> Development and testing is done in the latest version of Google Chrome, but Vizit uses HTML5 Boilerplate, Twitter Bootstrap, Modernizr, and more to accommodate as many devices and browsers as possible.

GeoJSON data is specified as a GET parameter like so: `/index.html?data=example.geojson`

***

## Advanced Features

Vizit looks for keywords in the properties of Feature objects. These keywords affect the look of the resulting visualization. Each property is listed alphabetically below.

* `image` -- content to be displayed in a popup ([Base64](https://en.wikipedia.org/wiki/Base64)-encoded string)
* `marker` -- string signifying what type of marker to create (`"Marker"` and `"CircleMarker"` are currently supported.)
* `markerOptions` -- object containing [Leaflet Marker Options](https://leafletjs.com/reference.html#marker-options) or [Leaflet Path Options](https://leafletjs.com/reference.html#path-options) for styling the [Marker](https://leafletjs.com/reference.html#marker) or [CircleMarker](https://leafletjs.com/reference.html#circlemarker) object, respectively, that represents the Feature (depending on the value of `marker`)
* `radius` -- floating point number representing an area around the Feature's Geometry (in meters)
* `radiusOptions` -- object containing [Leaflet Path Options](https://leafletjs.com/reference.html#path-options) for styling the [circle](https://leafletjs.com/reference.html#circle) that represents the radius (`radiusOptions` are only rendered if `radius` is specified.)
* `related` -- GeoJSON FeatureCollection of locally-related data
* `source` -- origin of `text` and `image` content
* `text` -- string to be displayed in a popup (Unicode encoding supported)
* `time` -- string produced by `JSON.stringify()` ([ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format)

***
