<template>
  <div class="v-slider-item">
    {{ sliderItems }}
  </div>
</template>

<script>
export default {
  name: 'v-slider-item',
  props: {
    sliderItems: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

<style scoped>

</style>
