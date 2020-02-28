<template>
  <div class="v-slider">
    <div class="v-slider-wrapper"
         :style="{'margin-left': '-' + (100 * this.currentSlideIndex) + '%'}"
    >
      <vsliderItem
        v-for="slide in sliderItems"
        :key="slide.id"
        :slide="slide"
        :imageSlide="true"
      >
        <div>{{ slide.id }}</div>
        <div>{{ slide.name }}</div>
      </vsliderItem>
    </div>
    <div class="v-slider-btns">
      <button class="v-slider-btns__btn"
              @click="prevSlide()"
      >Prev</button>
      <button class="v-slider-btns__btn"
              @click="nextSlide()"
      >Next</button>
    </div>
  </div>
</template>

<script>
import vsliderItem from './v-slider-item.vue';

export default {
  name: 'v-slider',
  components: {
    vsliderItem,
  },
  data() {
    return {
      currentSlideIndex: 0,
    };
  },
  props: {
    sliderItems: {
      type: Array,
      default: () => [],
    },
    interval: {
      type: Number,
      default: 0,
    },
  },
  methods: {
    prevSlide() {
      if (this.currentSlideIndex > 0) {
        this.currentSlideIndex--;
      }
    },
    nextSlide() {
      if (this.currentSlideIndex >= this.sliderItems.length - 1) {
        this.currentSlideIndex = 0;
      } else {
        this.currentSlideIndex++;
      }
    },
  },
  mounted() {
    const vm = this;
    if (this.interval > 0) {
      setInterval(() => {
        vm.nextSlide();
      }, vm.interval);
    }
  },
};
</script>

<style scoped lang="scss">
  .v-slider {
    max-width: 300px;
    margin: 0 auto;
    overflow: hidden;
    &-wrapper {
      display: flex;
      transition: all .3s ease-in;
    }
    &-btns {
      display: flex;
      justify-content: space-around;
      &__btn {
        height: 30px;
        background: #7f8080;
        min-width: 100px;
        cursor: pointer;
        transition: all .3s ease-in;
        border: none;
        color: white;
        &:hover {
          background: white;
          color: black;
          border: 1px solid #7f8080;
        }
      }
    }
  }
</style>
