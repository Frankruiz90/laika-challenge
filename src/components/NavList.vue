<template class="col-12">
  <v-toolbar class="nav-list hidden-md-and-down" width="100%" dense>
    <div class="text-center">
      <v-menu
        open-on-hover
        button
        offset-y
        v-for="(menu, i) in menuList"
        :key="i"
      >
        <template v-slot:activator="{ on, attrs }">
          <v-btn v-bind="attrs" v-on="on" text>
            <v-img contain :src="menu.img" alt="" />
            {{ menu.title }}
            <v-icon v-if="menu.title !== 'blog'">mdi-chevron-right</v-icon>
          </v-btn>
        </template>

        <v-list v-if="menu.title !== 'blog'">
          <v-list-item
            v-for="(item, index) in items"
            :key="index"
            link
            href="https://www.google.com"
          >
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
      <v-btn text href="https://blog.laika.com.co/"> Blog </v-btn>
      <v-btn
        rounded
        color="yellow"
        href="https://laika.com.co/laika_member/bog"
      >
        AQUIÉRELA YA
      </v-btn>
    </div>
  </v-toolbar>
</template>

<script>
import imgDog from "../assets/dog_mc.svg";
import imgCat from "../assets/cat_mc_s.svg";
export default {
  data: () => ({
    menuList: [
      { title: "Compra para perro", img: imgDog },
      { title: "Compra para gato", img: imgCat },
      { title: "Ofertas" },
      { title: "Servicios" },
    ],
    items: [
      { title: "Alimento" },
      { title: "Snacks" },
      { title: "Farmapet" },
      { title: "Cuidado e Higiene" },
      { title: "Juguetes" },
      { title: "Accesorios" },
      { title: "Para PetLovers" },
    ],
  }),
};
</script>

<style lang="scss" scoped>
.nav-list {
  position: fixed;
  z-index: 1;
}
</style>
