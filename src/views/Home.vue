<template>
  <div>
    <carousel />
    <categories />
    <feature-brands />
  </div>
</template>

<script>
import Carousel from "../components/Carousel.vue";
import Categories from "../components/Categories.vue";
import FeatureBrands from "../components/FeatureBrands.vue";

export default {
  name: "Home",

  components: {
    Carousel,
    Categories,
    FeatureBrands,
  },
};
</script>
