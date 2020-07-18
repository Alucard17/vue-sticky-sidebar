<template>
  <div ref="stickySidebar">
    <div class="sidebar__inner">
      <slot></slot>
    </div>
  </div>
</template>

<script>
import StickySidebar from "sticky-sidebar-v2";
export default {
  name: "vue-sticky-sidebar",
  props: {
    rootClass: {
        type: String,
        default: ''
    },
    topSpacing: {
      type: [Number, Function],
      default: 0
    },
    bottomSpacing: {
      type: [Number, Function],
      default: 0
    },
    containerSelector: {
      type: [String, Boolean],
      default: false
    },
    innerWrapperSelector: {
      type: String,
      default: ".inner-wrapper-sticky"
    },
    stickyClass: {
      type: [String, Boolean],
      default: false
    },
    resizeSensor: {
      type: Boolean,
      default: true
    },
    minWidth: {
      type: Number,
      default: 0
    }
  },
  data() {
    return {
      stickySidebar: null
    };
  },
  mounted() {
    this.stickySidebar = new StickySidebar(this.$refs.stickySidebar, {
      topSpacing: this.topSpacing,
      bottomSpacing: this.bottomSpacing,
      containerSelector: this.containerSelector,
      innerWrapperSelector: this.innerWrapperSelector,
      stickyClass: this.stickyClass,
      resizeSensor: this.resizeSensor,
      minWidth: this.minWidth
    });
  }
};
</script>
