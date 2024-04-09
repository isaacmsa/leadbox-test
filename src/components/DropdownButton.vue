<template>
  <div
    @mouseenter="enterDrop"
    @mouseleave="leaveDrop"
    :class="['relative h-full flex ', customClass]"
  >
    <button
      @mouseenter="enterDrop"
      @mouseleave="leaveDrop"
      class="text-sm font-medium uppercase mx-4 lg:mx-10 hover:font-bold"
      type="button"
    >
      {{ title }}
    </button>

    <div
      class="absolute top-20 right-2 pt-6 pb-5 px-6 w-56 bg-white shadowDrop z-20"
      v-if="isVisible"
      @mouseenter="enterDrop"
      @mouseleave="leaveDrop"
    >
      <slot name="drop"></slot>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    customClass: String,
  },
  data() {
    return {
      isVisible: false,
    }
  },
  methods: {
    enterDrop() {
      this.isVisible = true
    },
    leaveDrop() {
      this.isVisible = false
    },
  },
}
</script>

<style>
.shadowDrop {
  box-shadow: 0px 4px 10px 0px #00000026;
}
</style>
