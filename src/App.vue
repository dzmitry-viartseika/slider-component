<template>
  <div id="app">
    <vslider></vslider>
    <vsliderItem :sliderItems="sliderItems"></vsliderItem>
  </div>
</template>

<script>
import vslider from './components/v-slider.vue';
import vsliderItem from './components/v-slider-item.vue';

export default {
  name: 'App',
  components: {
    vslider,
    vsliderItem,
  },
  data() {
    return {
      sliderItems: [
        {
          id: 1,
          name: 'image1',
          img: 'img1.png',
        },
        {
          id: 2,
          name: 'image2',
          img: 'img2.png',
        },
        {
          id: 3,
          name: 'image3',
          img: 'img3.png',
        },
        {
          id: 4,
          name: 'image4',
          img: 'img4.png',
        },
      ],
    };
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
