<template>
  <swiper>
    <swiper-item v-for="item in banners" :key="item.background">
      <a :href="item.link">
        <img :src="item.image" alt="" @load="imageLoad" />
      </a>
    </swiper-item>
  </swiper>
</template>

<script>
import { Swiper, SwiperItem } from "components/common/swiper";
export default {
  name: "HomeSwiper",
  props: {
    banners: {
      type: Array,
      default() {
        return [];
      },
    },
  },
  data() {
    return {
      isLoad: false,
    };
  },
  methods: {
    imageLoad() {
      if (!this.isLoad) {
        // console.log("image");
        this.$emit("swiperImageLoad");
        this.isLoad = true;
      }
    },
  },
  components: {
    Swiper,
    SwiperItem,
  },
};
</script>

<style scoped>
</style>
