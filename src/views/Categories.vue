<template>
  <v-container>
    <h1 class="text-center mt-3">Categorías</h1>
    <v-row class="my-5">
      <v-col v-for="categoria in $store.state.games.categoriasData" :key="categoria.id" cols="12" sm="3" md="4">
        <CategoriesCard :value="categoria"/>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Categorias",
  components: {
    CategoriesCard: () => import("../components/Categories/CategoriesCard.vue")
  },
  mounted(){
    this.$store.dispatch("games/getAllCategorias")
  }
};
</script>

<style>
</style>
