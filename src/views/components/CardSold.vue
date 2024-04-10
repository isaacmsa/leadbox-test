<template>
  <div :class="['relative', image.id === 1 ? 'md:mr-4 lg:mr-0' : '']">
    <div class="absolute bg-[#F2F2F2] opacity-80 pt-2">
      <h5 class="font-extrabold text-xl">2016 Tesla Model X P90D Ludicrous</h5>
    </div>
    <img class="w-64 h-64 md:w-80 md:h-80" :src="image.src" :alt="image.name" />

    <div class="w-28 absolute bottom-0 bg-[#333333]">
      <span class="font-extrabold text-white text-xl uppercase">sold</span>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    image: Object,
  },
}
</script>

<style></style>
