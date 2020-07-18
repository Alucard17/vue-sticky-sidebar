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
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras tempus id leo et aliquam. Proin consectetur ligula vel neque cursus laoreet. Nullam dignissim, augue at consectetur pellentesque, metus ipsum interdum sapien, quis ornare quam enim vel ipsum.</p>

        <p>In congue nunc vitae magna tempor ultrices. Cras ultricies posuere elit. Nullam ultrices purus ante, at mattis leo placerat ac. Nunc faucibus ligula nec lorem sodales venenatis. Curabitur nec est condimentum, blandit tellus nec, semper arcu. Nullam in porta ipsum, non consectetur mi. Sed pharetra sapien nisl. Aliquam ac lectus sed elit vehicula scelerisque ut vel sem. Ut ut semper nisl.</p>

        <p>Curabitur rhoncus, arcu at placerat volutpat, felis elit sollicitudin ante, sed tempus justo nibh sed massa. Integer vestibulum non ante ornare eleifend. In vel mollis dolor.</p>
      </div>
    </div>

    <footer>
      <p>Very Tall Footer</p>
    </footer>
  </div>
</template>

<script>
import vueStickySidebar from "../src/vue-sticky-sidebar.vue";

export default {
  name: "ServeDev",
  components: {
    "vue-sticky-sidebar": vueStickySidebar
  }
};
</script>

	<style>
*,
*:before,
*:after {
  box-sizing: border-box;
}

body {
  font-family: Arial;
}

header {
  color: #888;
}

header h1 {
  font-size: 30px;
}

.container {
  max-width: 700px;
  margin: 0 auto;
}

#content {
  border: 2px dotted green;
  padding: 18px;
  margin-left: 215px;
  min-height: 2000px;
  color: darkgrey;
}

.sidebar {
  float: left;
  width: 200px;
  color: #ffbdbd;
  will-change: min-height;
}

.sidebar .sidebar__inner {
  border: 2px dotted red;
  padding: 10px;
  position: relative;
  transform: translate(0, 0);
  transform: translate3d(0, 0, 0);
  will-change: position, transform;
}

footer {
  height: 300px;
  height: 85vh;
  border: 2px dotted black;
  margin-top: 20px;
  text-align: center;
  color: #8e8d8d;
  background: rgba(0, 0, 0, 0.02);
  line-height: 300px;
  line-height: 95vh;
}

footer p {
  margin: 0;
}

.clearfix:after {
  display: block;
  content: "";
  clear: both;
}
</style>
