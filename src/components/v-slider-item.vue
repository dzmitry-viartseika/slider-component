<template>
  <div class="v-slider-item">
    {{ sliderItems }}
  </div>
</template>

<script>
export default {
  name: 'v-slider-item',
  props: {
    vsliderItem: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

<style scoped>

</style>
