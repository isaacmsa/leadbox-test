<template>
  <div>
    <h2 :class="['text-[#333333] font-bold text-4xl', styles]">{{ title }}</h2>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    styles: String,
  },
}
</script>

<style></style>
