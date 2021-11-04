# vue-zoomer

> Zoom the image or other thing with mouse or touch. Based on [https://github.com/jarvisniu/vue-zoomer/](https://github.com/jarvisniu/vue-zoomer/).


## Demo

- https://unpkg.com/@ikoncept/vue-zoomer@0.3.11/dist/demo/basic.html

## Usage

Install:

```bash
yarn add @ikoncept/vue-zoomer
```

Import:

```js
import Vue from 'vue'
import VueZoomer from '@ikoncept/vue-zoomer'

Vue.use(VueZoomer)
```

Usage:

```html
<VZoomer style="width: 500px; height: 500px; border: solid 1px silver;">
  <img
    src="./assets/landscape-1.jpg"
    style="object-fit: contain; width: 100%; height: 100%;"
  >
</VZoomer>
```

## API

### &lt;VZoomer&gt; Props

- `aspectRatio: number` - Calculated aspect ratio of image (always width / height). Without this limits won't work properly, default is 1 (square);
- `maxScale: number` - Maximum scale limit, default is 5;
- `minScale: number` - Minimum scale limit, default is 1;
- `zoomed: out boolean` - Whether zoomed in (scale equals to 1). `out` means the prop is a child to parent one-way binding. So there must have a `.sync` modifier.
- `pivot: 'cursor' | 'image-center'` - The pivot when zoom the content, default is `cursor`, can set to be `image-center`;
- `zoomingElastic: boolean` - Whether to use the elastic effect when reaching the max/min zooming bounds, default is `true`;
- `limitTranslation: boolean` - Whether to limit the content into the container, default is `true`;
- `singleClickToZoom: boolean` - Whether to zoom in/out the content by single click, default is `true`;
- `doubleClickToZoom: boolean` - Whether to zoom in/out the content by double click, default is `true`;
- `mouseWheelToZoom: boolean` - Whether to zoom in/out the content by mouse wheel, default is `true`;


### &lt;VZoomer&gt; Methods

- `reset()` - Reset the scale and translate to the initial state.
- `zoomIn(scale=2)` - Zoom in.
- `zoomOut(scale=0.5)` - Zoom out.

## License

MIT
