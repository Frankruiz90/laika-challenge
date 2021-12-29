<template>
  <div>
    <carousel />
    <categories />
    <feature-brands />
    <card-product />
  </div>
</template>

<script>
import Carousel from "../components/Carousel.vue";
import Categories from "../components/Categories.vue";
import FeatureBrands from "../components/FeatureBrands.vue";
import CardProduct from "../components/CardProduct.vue";

export default {
  name: "Home",

  components: {
    Carousel,
    Categories,
    FeatureBrands,
    CardProduct,
  },
};
</script>
