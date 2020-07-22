<template>
  <div ref="stickySidebar">
    <div class="inner-wrapper-sticky">
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
    stickyClass: {
      type: [String, Boolean],
      default: false
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
      innerWrapperSelector: '.inner-wrapper-sticky',
      stickyClass: this.stickyClass,
      minWidth: this.minWidth
    });
  }
};
</script>
