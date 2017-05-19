# Mapbox GL Traffic [![Build Status](https://travis-ci.org/mapbox/mapbox-gl-traffic.svg?branch=master)](https://travis-ci.org/mapbox/mapbox-gl-traffic) [![npm](https://img.shields.io/npm/v/@mapbox/mapbox-gl-traffic.svg)](https://www.npmjs.com/package/@mapbox/mapbox-gl-traffic)

Add a traffic toggle control to [Mapbox GL JS](https://github.com/mapbox/mapbox-gl-js).

[**:globe_with_meridians: Check the demo**](https://mapbox.github.io/mapbox-gl-traffic/)

![demo](https://raw.githubusercontent.com/lukasmartinelli/mapbox-gl-traffic/master/demo.gif)

## Usage

**mapbox-gl-traffic** is a [Mapbox GL JS plugin](https://www.mapbox.com/blog/build-mapbox-gl-js-plugins/) that you can easily add on top of your map. Check `index.html` for a complete example.

Make sure to include the CSS and JS files.

**When using NPM**

Check [how to use Mapbox GL JS in a module bundler](https://www.mapbox.com/mapbox-gl-js/api/).

```bash
npm install --save mapbox-gl @mapbox/mapbox-gl-traffic
```

```javascript
const mapboxgl = require('mapbox-gl')
const MapboxTraffic = require('@mapbox/mapbox-gl-traffic');
const map = new mapboxgl.Map({
    container: 'map',
    style: 'mapbox://styles/mapbox/traffic-night-v2',
    center: [-77.0259, 38.9010],
    zoom: 9
});
map.addControl(new MapboxTraffic());
```

## Examples

- [Mapbox Day Traffic](https://mapbox.github.io/mapbox-gl-traffic/examples/traffic-day.html)
- [Mapbox Night Traffic](https://mapbox.github.io/mapbox-gl-traffic/examples/traffic-night.html)
- [Mapbox Streets](https://mapbox.github.io/mapbox-gl-traffic/examples/mapbox-streets.html)
- [Mapbox Outdoors](https://mapbox.github.io/mapbox-gl-traffic/examples/mapbox-outdoors.html)
- [Mapbox Light](https://mapbox.github.io/mapbox-gl-traffic/examples/mapbox-light.html)
- [Mapbox Dark](https://mapbox.github.io/mapbox-gl-traffic/examples/mapbox-dark.html)

## API

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### MapboxTraffic

Create a new [Mapbox GL JS plugin](https://www.mapbox.com/blog/build-mapbox-gl-js-plugins/) that allows you to hide and show
traffic layers in your map and an optional toggle button.

**Parameters**

-   `options` **[object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** Options to configure the plugin.
    -   `options.showTraffic` **[boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** Show or hide traffic overlay by default. (optional, default `false`)
    -   `options.showTrafficButton` **[boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** Show a toggle button to turn traffic on and off. (optional, default `true`)
    -   `options.trafficSource` **[RegExp](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)** The traffic source regex used to determine whether a layer displays traffic or not. (optional, default `/mapbox-traffic-v\d/`)

## Develop

Run the linter and watch for changes to rebuild with browserify.

    npm install
    npm run test
    npm run watch

Create a minified standalone build.

    npm install
    npm run build
