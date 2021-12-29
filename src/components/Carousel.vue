<template>
  <div class=" mt-15 mt-lg-12">
    <v-carousel cycle height="187" hide-delimiter-background show-arrows>
      <v-carousel-item v-for="(slide, i) in slides" :key="i">
        <v-img contain :src="slide.src" />
      </v-carousel-item>
    </v-carousel>
  </div>
</template>

<script>
import carousel1 from "../assets/carousel1.jpg";
import carousel2 from "../assets/carousel2.jpg";
import carousel3 from "../assets/carousel3.jpg";
import carousel4 from "../assets/carousel4.jpg";
import carousel5 from "../assets/carousel5.jpg";
import carousel6 from "../assets/carousel6.jpg";
export default {
  data: () => ({
    slides: [
      { src: carousel1 },
      { src: carousel2 },
      { src: carousel3 },
      { src: carousel4 },
      { src: carousel5 },
      { src: carousel6 },
    ],
  }),
};
</script>

<style>
</style>