<template>
  <v-app-bar app color="#111111" dark flat class="px-8" v-if="isNotMobile">


    <v-spacer></v-spacer>
    <v-btn text @click="scroll('home')">Home</v-btn>
    <v-btn text @click="scroll('project')">Expériences</v-btn>
    <v-btn text @click="scroll('myskill')">COmpétences</v-btn>
    <v-btn text @click="scroll('section-projet')">Projets</v-btn>
    <v-btn text @click="scroll('footer')"> Contact</v-btn>
  </v-app-bar>  


</template>

<script>
export default {
  methods: {
    scroll(refName) {
      const element = document.getElementById(refName);
      element.scrollIntoView({ behavior: "smooth" });
    },
  },
  computed: {
   isNotMobile() {
      return this.$vuetify.breakpoint.smAndUp;
   }
}
};
</script>

<style>
</style>