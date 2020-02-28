<template>
  <div id="app">
    <vslider :sliderItems="sliderItems"
             :interval="2000"
    ></vslider>
  </div>
</template>

<script>
import vslider from './components/v-slider.vue';

export default {
  name: 'App',
  components: {
    vslider,
  },
  data() {
    return {
      sliderItems: [
        {
          id: 1,
          name: 'image1',
          img: 'https://cdn.pixabay.com/photo/2015/04/23/22/00/tree-736885__340.jpg',
        },
        {
          id: 2,
          name: 'image2',
          img: 'https://images.unsplash.com/photo-1503803548695-c2a7b4a5b875?ixlib=rb-1.2.1&w=1000&q=80',
        },
        {
          id: 3,
          name: 'image3',
          img: 'https://images.pexels.com/photos/34950/pexels-photo.jpg?auto=compress&cs=tinysrgb&dpr=1&w=500',
        },
        {
          id: 4,
          name: 'image4',
          img: 'https://www.istockphoto.com/resources/images/PhotoFTLP/NatureLandscapes-519760984.jpg',
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
