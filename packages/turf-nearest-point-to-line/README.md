# @turf/nearest-point-to-line

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

## nearestPointToLine

Returns the closest [point][1], of a [collection][2] of points, to a [line][3].
The returned point has a `dist` property indicating its distance to the line.

**Parameters**

-   `points` **([FeatureCollection][4] \| [GeometryCollection][5]&lt;[Point][6]>)** Point Collection
-   `line` **([Feature][7] \| [Geometry][8]&lt;[LineString][9]>)** Line Feature
-   `options` **[Object][10]?** Optional parameters
    -   `options.units` **[string][11]** unit of the output distance property, can be degrees, radians, miles, or kilometers (optional, default `'kilometers'`)
    -   `options.properties` **[Object][10]** Translate Properties to Point (optional, default `{}`)

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

Returns **[Feature][7]&lt;[Point][6]>** the closest point

## pt

Translate Properties to final Point, priorities:
1\. options.properties
2\. inherent Point properties
3\. dist custom properties created by NearestPointToLine

[1]: https://tools.ietf.org/html/rfc7946#section-3.1.2

[2]: https://tools.ietf.org/html/rfc7946#section-3.3

[3]: https://tools.ietf.org/html/rfc7946#section-3.1.4

[4]: https://tools.ietf.org/html/rfc7946#section-3.3

[5]: https://tools.ietf.org/html/rfc7946#section-3.1.8

[6]: https://tools.ietf.org/html/rfc7946#section-3.1.2

[7]: https://tools.ietf.org/html/rfc7946#section-3.2

[8]: https://tools.ietf.org/html/rfc7946#section-3.1

[9]: https://tools.ietf.org/html/rfc7946#section-3.1.4

[10]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object

[11]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String

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