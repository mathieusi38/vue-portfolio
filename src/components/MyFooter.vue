<template>
  <v-footer
    dark
    padless
    class="my-footer"
  >
    <v-card
      flat
      tile
      class=" white--text text-center my-footer-color"
    >
      <v-card-text>
        <v-btn
          v-for="(icon, index) in icons"
          :key="icon"
          class="mx-5 white--text social-icon"
          icon
          style="padding:25px;"
          :href=url[index]
        >
          <v-icon size="34px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-text>


    </v-card>
  </v-footer>
</template>


<script>
export default {
  name: "MyFooter",
  data: () => ({
    icons: ["mdi-twitter", "mdi-linkedin"],
    url: ["https://twitter.com/MathieuSiaud", "https://www.linkedin.com/in/mathieu-siaud-a971a9198"],
  }),
  components: {
  },
};
</script>

<style scoped>

.my-footer {
  background: inherit;
  margin: auto;
}

.my-footer-color{
  background: inherit;
}

.social-icon:hover{
  background: #B71C1C ;
  border-radius: 25px;
  padding: 30px;
}

.theme--dark.v-footer {
  background-color: inherit;
  color: #FFFFFF;
}
</style>