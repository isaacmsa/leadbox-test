<template>
  <div
    :class="[
      'mb-3 md:mr-10 xl:mr-4',
      !data.isResponsive ? 'md:hidden lg:block' : '',
      data.id === 1 ? 'md:mr-10' : '',
    ]"
  >
    <figure class="relative mb-3">
      <img
        :src="data.img"
        class="w-80 md:w-96 lg:w-full h-48 md:h-52"
        :alt="data.img"
      />
      <img
        src="../../../public/assets/figures/rectangle-card.png"
        class="md:hidden lg:flex absolute -bottom-0.5 w-80 lg:w-full"
        alt="rectangle"
      />
    </figure>
    <div>
      <div class="mb-3">
        <h3 class="text-2xl md:text-4xl font-semibold text-black">
          {{ data.title }}
        </h3>
      </div>
      <span class="text-sm font-normal text-[#081534]">{{
        data.subTitle
      }}</span>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    data: Object,
  },
}
</script>

<style></style>
