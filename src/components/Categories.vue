<template>
  <div class="pt-4">
    <v-container class="categories">
      <div class="categories-title mb-4">
        <h3>Categoría</h3>
      </div>
      <v-row justify="center" class="px-0 px-lg-6">
        <v-col
          class="col-12 col-lg-3"
          v-for="(categorie, index) in categories"
          :key="index"
        >
          <v-btn class="categories-btn" :href="categorie.url" block>
            <v-img
              class="categories-icon me-2"
              contain
              :src="categorie.icon"
              alt=""
            />
            {{ categorie.title }}
          </v-btn>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import logo from "../assets/icon.png";

export default {
  data: () => ({
    categories: [
      { title: "Anilento", icon: logo, url: "google.com" },
      { title: "Snacks", icon: logo, url: "google.com" },
      { title: "Farmapet", icon: logo, url: "google.com" },
      { title: "Cuidado e higiene", icon: logo, url: "google.com" },
      { title: "Juguetes", icon: logo, url: "google.com" },
      { title: "Accesorios", icon: logo, url: "google.com" },
      { title: "Para pet lovers", icon: logo, url: "google.com" },
    ],
  }),
};
</script>

<style lang="scss" >
.categories {
  &-title {
    h3 {
      color: rgb(96, 62, 133);
    }
  }
  &-btn {
    .v-btn__content {
      flex: 0 0 auto !important;
    }
  }
  &-icon {
    height: 20px;
    width: 20px;
    border-color: violet;
  }
}
</style>