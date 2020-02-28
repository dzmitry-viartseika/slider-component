<template>
  <div class="v-slider-item"
  >
    <img class="v-slider-item-wrapper__slide-img" :src="slide.img" alt="" v-if="imageSlide">
    <div v-else>
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'v-slider-item',
  props: {
    slide: {
      type: Object,
      default: () => {},
    },
    imageSlide: {
      type: Boolean,
      default: true,
    },
  },
};
</script>

<style scoped lang="scss">
 .v-slider-item {
   min-width: 300px;
    & img {
      max-width: 300px;
      min-width: 300px;
      height: 200px;
      overflow: hidden;
    }
 }
</style>
