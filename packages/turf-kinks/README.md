# @turf/kinks

# kinks

Takes a [polygon](http://geojson.org/geojson-spec.html#polygon) and returns [points](http://geojson.org/geojson-spec.html#point) at all self-intersections.

**Parameters**

-   `polygon` **([Feature](http://geojson.org/geojson-spec.html#feature-objects)&lt;[Polygon](http://geojson.org/geojson-spec.html#polygon)> | [Polygon](http://geojson.org/geojson-spec.html#polygon))** input polygon

**Examples**

```javascript
var poly = {
  "type": "Feature",
  "properties": {},
  "geometry": {
    "type": "Polygon",
    "coordinates": [[
      [-12.034835, 8.901183],
      [-12.060413, 8.899826],
      [-12.03638, 8.873199],
      [-12.059383, 8.871418],
      [-12.034835, 8.901183]
    ]]
  }
};

var kinks = turf.kinks(poly);

var resultFeatures = kinks.intersections.features.concat(poly);
var result = {
  "type": "FeatureCollection",
  "features": resultFeatures
};

//=result
```

Returns **[FeatureCollection](http://geojson.org/geojson-spec.html#feature-collection-objects)&lt;[Point](http://geojson.org/geojson-spec.html#point)>** self-intersections

---

This module is part of the [Turfjs project](http://turfjs.org/), an open source
module collection dedicated to geographic algorithms. It is maintained in the
[Turfjs/turf](https://github.com/Turfjs/turf) repository, where you can create
PRs and issues.

### Installation

Install this module individually:

```sh
$ npm install @turf/kinks
```

Or install the Turf module that includes it as a function:

```sh
$ npm install @turf/turf
```
