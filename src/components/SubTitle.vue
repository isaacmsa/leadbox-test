<template>
  <div :class="styleContainer">
    <span :class="styleText">{{ subTitle }}</span>
  </div>
</template>

<script>
export default {
  props: {
    subTitle: String,
    styleText: String,
    styleContainer: String,
  },
}
</script>

<style></style>
