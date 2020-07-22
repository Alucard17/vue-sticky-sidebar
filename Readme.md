## Vue.js component implementing the [sticky-sidebar-v2](https://github.com/blixhavn/sticky-sidebar-v2) library.
![Version](https://badgen.net/npm/v/vue-sticky-sidebar)
![Downloads/Week](https://badgen.net/npm/dw/vue-sticky-sidebar)
![Minified Bundlesize](https://badgen.net/bundlephobia/min/vue-sticky-sidebar)
![Minified Gzipped Bundlesize](https://badgen.net/bundlephobia/minzip/vue-sticky-sidebar)

## Installation
Using npm:
```shell
$ npm install --save vue-sticky-sidebar
```
Using yarn:
```shell
$ yarn add vue-sticky-sidebar
```

## Usage
```html
<template>
  <div id="app">
    <header>
      <div class="container">
        <h1>Site Title</h1>
      </div>
    </header>

    <div class="container clearfix">
      <vue-sticky-sidebar class="sidebar" containerSelector=".container" innerWrapperSelector='.sidebar__inner'>
            <p>This is sticky column</p>
      </vue-sticky-sidebar>
      <div id="content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras tempus id leo et aliquam. Proin consectetur ligula vel neque cursus laoreet. Nullam dignissim, augue at consectetur pellentesque, metus ipsum interdum sapien, quis ornare quam enim vel ipsum.</p> dolor.</p>
      </div>
    </div>

    <footer>
      <p>Very Tall Footer</p>
    </footer>
  </div>
</template>



<script>
import vueStickySidebar from "vue-sticky-sidebar";

export default {
  name: "ServeDev",
  components: {
    "vue-sticky-sidebar": vueStickySidebar
  }
};
</script>
```

## Props
| Name                | Type               |  Default                 |  Description                                                                          |
|---------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------|
| topSpacing          |  Numeric, Function |  0                       | Additional top spacing of the element when it becomes sticky.                         |
| bottomSpacing       |  Numeric, Function |  0                       | Additional bottom spacing of the element when it becomes sticky.                      |
| containerSelector   |  String, False     |  false                   | Container sidebar selector to know what the beginning and end of sticky element.      |
| innerWrapperSelector|  String            |  .inner-wrapper-sticky   | Inner wrapper selector.                                                               |
| stickyClass         |  String, False     |  is-affixed              | The name of CSS class to apply to elements when they have become stuck.               |
| resizeSensor        |  Boolean           |  true                    | Detect when sidebar and its container change height so re-calculate their dimensions. |
| minWidth            |  Numeric           |   0                      | The sidebar returns to its normal position if its width below this value.             |

Find more reference at official [sticky-sidebar-v2](https://github.com/blixhavn/sticky-sidebar-v2).
## Todo
- Add Events
