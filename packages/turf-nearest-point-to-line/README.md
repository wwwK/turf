# @turf/nearest-point-to-line

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

## nearestPointToLine

Returns the closest [point](https://tools.ietf.org/html/rfc7946#section-3.1.2), of a [collection](https://tools.ietf.org/html/rfc7946#section-3.3) of points, to a [line](https://tools.ietf.org/html/rfc7946#section-3.1.4).
The returned point has a `dist` property indicating its distance to the line.

**Parameters**

-   `points` **([FeatureCollection](https://tools.ietf.org/html/rfc7946#section-3.3) \| [GeometryCollection](https://tools.ietf.org/html/rfc7946#section-3.1.8)&lt;[Point](https://tools.ietf.org/html/rfc7946#section-3.1.2)>)** Point Collection
-   `line` **([Feature](https://tools.ietf.org/html/rfc7946#section-3.2) \| [Geometry](https://tools.ietf.org/html/rfc7946#section-3.1)&lt;[LineString](https://tools.ietf.org/html/rfc7946#section-3.1.4)>)** Line Feature
-   `options` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)?** Optional parameters
    -   `options.units` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** unit of the output distance property, can be degrees, radians, miles, or kilometers (optional, default `'kilometers'`)
    -   `options.properties` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** Translate Properties to Point (optional, default `{}`)

**Examples**

```javascript
var pt1 = turf.point([0, 0]);
var pt2 = turf.point([0.5, 0.5]);
var points = turf.featureCollection([pt1, pt2]);
var line = turf.lineString([[1,1], [-1,1]]);

var nearest = turf.nearestPointToLine(points, line);

//addToMap
var addToMap = [nearest, line];
```

Returns **[Feature](https://tools.ietf.org/html/rfc7946#section-3.2)&lt;[Point](https://tools.ietf.org/html/rfc7946#section-3.1.2)>** the closest point

## pt

Translate Properties to final Point, priorities:
1\. options.properties
2\. inherent Point properties
3\. dist custom properties created by NearestPointToLine

<!-- This file is automatically generated. Please don't edit it directly:
if you find an error, edit the source file (likely index.js), and re-run
./scripts/generate-readmes in the turf project. -->

---

This module is part of the [Turfjs project](http://turfjs.org/), an open source
module collection dedicated to geographic algorithms. It is maintained in the
[Turfjs/turf](https://github.com/Turfjs/turf) repository, where you can create
PRs and issues.

### Installation

Install this module individually:

```sh
$ npm install @turf/nearest-point-to-line
```

Or install the Turf module that includes it as a function:

```sh
$ npm install @turf/turf
```
