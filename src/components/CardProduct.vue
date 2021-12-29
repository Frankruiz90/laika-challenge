<template>
  <div>
    <v-contanier align="center">
      <v-row justify="center">
        <div v-for="(card, index) in cards" :key="index" class="card">
          <v-card :loading="loading" class="mx-4 my-12" max-width="270">
            <v-img contain height="150" :src="card.img" class="pa-5"></v-img>

            <v-card-title>{{ card.title }}</v-card-title>

            <v-card-text>
              <v-row align="center" class="mx-0">
                <v-rating
                  :value="card.value"
                  color="amber"
                  dense
                  half-increments
                  readonly
                  size="14"
                ></v-rating>

                <div class="grey--text ms-4">{{ card.value }}</div>
              </v-row>

              <div class="my-4 text-subtitle-1">Antes $ {{ card.price }}</div>
              <div class="my-4 text-subtitle-1">
                Ahora $ {{ card.priceNew }}
              </div>
            </v-card-text>

            <v-divider class="mx-4"></v-divider>

            <v-card-actions>
              <v-btn color="deep-purple lighten-2" block dark @click="reserve">
                <v-icon>mdi-cart-outline</v-icon>
                Añadir al carrito
              </v-btn>
            </v-card-actions>
          </v-card>
        </div>
      </v-row>
    </v-contanier>
  </div>
</template>

<script>
import imgCard from "../assets/img-card.png";

export default {
  data: () => ({
    cards: [
      {
        title: "Furminator - Deslanador Perro Mediano Pelo Largo.",
        img: imgCard,
        value: 5,
        price: "5.500",
        priceNew: "4.500",
      },
      {
        title: "Furminator - Deslanador Perro Mediano Pelo Largo.",
        img: imgCard,
        value: 5,
        price: "5.500",
        priceNew: "4.500",
      },
      {
        title: "Furminator - Deslanador Perro Mediano Pelo Largo.",
        img: imgCard,
        value: 5,
        price: "5.500",
        priceNew: "4.500",
      },
      {
        title: "Furminator - Deslanador Perro Mediano Pelo Largo.",
        img: imgCard,
        value: 5,
        price: "5.500",
        priceNew: "4.500",
      },
      {
        title: "Furminator - Deslanador Perro Mediano Pelo Largo.",
        img: imgCard,
      },
    ],
  }),
};
</script>
<style lang="scss" >
</style>