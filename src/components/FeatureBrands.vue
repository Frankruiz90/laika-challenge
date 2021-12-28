<template>
  <div class="my-5 brands">
    <v-container>
      <div class="brands-title mb-4">
        <h3>Marcas destacadas</h3>
      </div>
      <v-sheet class="mx-auto" max-width="800">
        <v-slide-group multiple show-arrows>
          <v-slide-item
            v-for="(brand, index) in brands"
            :key="index"
            v-slot="{ active, toggle }"
          >
            <v-col class="">
              <div
                class="brands-rounded elevation-5"
                :input-value="active"
                @click="toggle"
              >
                <v-img contain :src="brand.icon"> </v-img>
              </div>
            </v-col>
          </v-slide-item>
        </v-slide-group>
      </v-sheet>
    </v-container>
  </div>
</template>

<script>
import logo from "../assets/marcas.png";

export default {
  data: () => ({
    brands: [
      { title: "Anilento", icon: logo, url: "google.com" },
      { title: "Snacks", icon: logo, url: "google.com" },
      { title: "Farmapet", icon: logo, url: "google.com" },
      { title: "Cuidado e higiene", icon: logo, url: "google.com" },
      { title: "Juguetes", icon: logo, url: "google.com" },
      { title: "Accesorios", icon: logo, url: "google.com" },
      { title: "Para pet lovers", icon: logo, url: "google.com" },
      { title: "Farmapet", icon: logo, url: "google.com" },
      { title: "Cuidado e higiene", icon: logo, url: "google.com" },
      { title: "Juguetes", icon: logo, url: "google.com" },
      { title: "Accesorios", icon: logo, url: "google.com" },
      { title: "Para pet lovers", icon: logo, url: "google.com" },
    ],
  }),
};
</script>

<style lang="scss">
.brands {
  &-title {
    h3 {
      color: rgb(96, 62, 133);
    }
  }
  &-rounded {
    height: 100px;
    width: 100px;
    border-radius: 100%;
    cursor: pointer;
    img {
      border-radius: 100%;
      object-fit: contain;
    }
    &:hover {
      height: 110px;
      width: 110px;
      transition-property: all;
      transition-duration: 0.2s;
    }
  }
}
</style>