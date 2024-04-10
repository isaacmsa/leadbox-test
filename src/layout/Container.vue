<template>
  <div :class="customClass">
    <slot name="container"></slot>
  </div>
</template>

<script>
export default {
  props: {
    customClass: String,
  },
}
</script>

<style></style>
