<template>
  <v-app>
    <v-app-bar app color="#603e85" class="pa-0 nav-bar" height="100" dark>
      <v-row no-gutters>
        <v-col cols="1">
          <div class="d-block pt-3">
            <v-img
              alt="assets\logo.png"
              class="shrink mr-2"
              contain
              src="../src/assets/LaikaMascotas.svg"
              transition="scale-transition"
              width="40"
            />
            <p class="mb-0">Laika</p>
          </div>
        </v-col>
        <v-col cols="6" class="pt-4 hidden-md-and-down">
          <div class="d-flex aling-center">
            <v-text-field
              placeholder="Encuentra lo mejor para tu mascota"
              outlined
              dense
              background-color="white"
              color="black"
              light
            >
              <v-icon slot="append" color="grey"> mdi-magnify </v-icon>
            </v-text-field>
          </div>
        </v-col>
        <v-col  class="pt-4 col-2 col-md-1">
          <div class="d-flex aling-center justify-center">
            <v-img
              src="../src/assets/Flag_of_Colombia.png"
              class="shrink mr-2"
              contain
              width="40"
              height="40"
            ></v-img>
          </div>
        </v-col>
        <v-col class="pt-4 col-2 col-md-1">
          <div class="d-flex aling-center">
            <v-select
              v-model="city"
              :items="cities"
              menu-props="auto"
              label="Bog"
              hide-details
              single-line
            ></v-select>
          </div>
        </v-col>
        <v-col  class="col-4 col-md-2">
          <div class="d-flex align-center justify-center bar-user">
            <a href="" class="bar__link">
              <div class="bar__link-icon me-2">
                <v-icon slot="append" color="white">
                  mdi-account-outline
                </v-icon>
              </div>
              <div class="d-flex align-center">Mi cuenta</div>
            </a>
          </div>
        </v-col>
        <v-col  class="col-2 col-md-1">
          <div class="d-flex align-center justify-center bar-user">
            <v-badge color="red" :content="products">
              <div class="d-flex align-center justify-center bar-user">
                <a href="" class="bar__link">
                  <div class="">
                    <v-icon slot="append" color="white">
                      mdi-cart-outline
                    </v-icon>
                  </div>
                </a>
              </div>
            </v-badge>
          </div>
        </v-col>
        <v-col cols="12" class="pt-4 hidden-lg-and-up show-md-and-down">
          <div class="d-flex aling-center">
            <v-text-field
              placeholder="Encuentra lo mejor para tu mascota"
              outlined
              dense
              background-color="white"
              color="black"
              light
            >
              <v-icon slot="append" color="grey"> mdi-magnify </v-icon>
            </v-text-field>
          </div>
        </v-col>
      </v-row>
    </v-app-bar>
    <v-main class="">
      <nav-list class="mb-5"></nav-list>

      <router-view />
    </v-main>
  </v-app>
</template>

<script>
import NavList from "../src/components/NavList.vue";
export default {
  name: "App",

  data: () => ({
    city: "",
    products: 1,
    cities: ["Medellin", "Bogota", "Pereira", "Cali"],
  }),
  components: {
    NavList,
  },
};
</script>

<style lang="scss">
.nav-bar {
  height: 100px;
  @media (max-width: 1264px) {
    height: 160px !important;
    .v-toolbar__content {
      height: 160px !important;
    }
  }
}
.bar-user {
  height: 100%;
}
.bar__link {
  text-decoration: none;
  display: flex;
  color: white;
  &-icon {
    height: 35px;
    width: 35px;
    background-color: #8358b3d5;
    border-radius: 100%;
    display: flex;
    justify-content: center;
  }
}
</style>
