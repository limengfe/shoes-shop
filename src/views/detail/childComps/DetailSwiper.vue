<template>
  <div class="detai-swiper">
    <swiper class="swiper1">
      <swiper-item v-for="item in topImages" :key="item">
        <img :src="item" />
      </swiper-item>
    </swiper>
  </div>
</template>

<script>
import { Swiper, SwiperItem } from "components/common/swiper";

export default {
  name: "DetailSwiper",
  components: { Swiper, SwiperItem },
  props: {
    topImages: {
      type: Array,
      default() {
        return [];
      },
    },
  },
};
</script>

<style scoped>
.swiper1 {
  height: 300px;
  overflow: hidden;
}
</style>