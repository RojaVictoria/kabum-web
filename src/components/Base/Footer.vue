<template>
  <v-footer app dark padless absolute>
    <v-card class="flex" flat tile>
      <v-card-title class="blue accent-4">
        <v-img src="../../assets/kabum.png" max-width="125" />

        <v-spacer></v-spacer>

        <v-btn v-for="icon in icons" :key="icon" class="mx-4" dark icon>
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-title>

      <v-card-text class="orange lighten-1 py-2 white--text text-center text-font">
        {{ new Date().getFullYear() }} - <strong>KABUM!</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  name: "Footer",
  data: () => ({
    icons: ["mdi-instagram", "mdi-facebook"],
  }),
};
</script>

<style scoped>
.text-font {
    font-family: 'Outfit', sans-serif;
}
</style>
