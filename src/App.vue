<template>
  <v-app
    id="home"
    :style="{ background: $vuetify.theme.themes.dark.background }"
  >
    <nav-bar />
    <v-container fluid top>
      <v-row class="spacing-playground">
        <!-- Presentation -->
        <v-col cols="12" sm="6" >
          <v-img src="mathieu.png" contain max-height="500"></v-img>
        </v-col>
        <v-col cols="12" sm="6" class="text-center text-sm-left ">
          <h5 class="red--text text--darken-4 top title">Mathieu Siaud</h5>
          <h1 class="white--text">Developpeur web</h1>
          <p class="grey--text">
            Et si je commençais par me présenter ? <br />
            Passionné par le monde du développement web, <br>
             je suis actuellement en master ingénierie du web afin d'approfondir mes connaissances.
          </p>
          <v-btn tile color="#A7121D" dark href="#project"> Mes expériences </v-btn>
        </v-col>
        <!-- Ecole -->
        <v-col cols="12" class="padd">
          <div class="first" id="project">
            <v-row>
              <v-col cols="12">
                <div class="child bgColor1 mb-6 mb-sm-0">
                  <h3 class="ml-3 mt-4 red--text">Bac +5</h3>
                  <h3 class="white--text ml-3 mt-4">Mastère Ingénierie du Web</h3>
                  <p class="grey--text ml-3 mt-6">
                    Solution de versioning  <br />
                    UX et UI <br />
                    Technologie web et Frameworks <br />
                    Référencement <br />
                    Challenge de projet WEB <br />
                  </p>
                </div>
                <div class="child bgColor1 mb-6 mb-sm-0">
                  <h3 class="ml-3 mt-4 red--text">Bac +3</h3>
                  <h3 class="white--text ml-3 mt-4">Licence pro Metinet</h3>
                  <p class="grey--text ml-3 mt-6">
                    Technologie web et Frameworks <br />
                    Référencement <br />
                    Accessibilité et Ergonomie <br />
                    Graphisme <br />
                    Communication <br />
                  </p>
                </div>
                <div class="child bgColor1">
                  <h3 class="ml-3 mt-4 red--text">Bac +2</h3>
                  <h3 class="white--text ml-3 mt-4">Dut MMI</h3>
                  <p class="grey--text ml-3 mt-6">
                    Intégration web <br />
                    Réseaux <br />
                    Infographie <br />
                    UX et UI <br />
                    Communication <br />
                  </p>
                </div>
              </v-col>
              <!-- Exp -->
              <v-col cols="12" class="mt-5">
                <div class="child1">
                  <h1 class="red--text text--darken-4 mt-4 number">+3 ans</h1>
                  <h3 class="white--text mt-4">d'expérience professionnelle</h3>
                </div>
                <div class="child2 mRight mb-10 mb-sm-0">
                  <v-row>
                    <v-col cols="12" class="childcol">
                      <div class="child2 mButton padding bgColor1">
                        <h1 class="red--text text--darken-4">Probesys</h1>
                        <p class="grey--text">Drupal, Git, Sass, Php, Jquery</p>
                      </div>
                    </v-col>
                  </v-row>
                </div>
                <div class="child2">
                  <v-row>
                    <v-col cols="12" class="childcol">
                      <div class="child2 mButton padding bgColor1">
                        <h1 class="red--text text--darken-4">Eolas</h1>
                        <p class="grey--text">Git, Javascript, Php, Sass, Html</p>
                      </div>
                    </v-col>
                  </v-row>
                </div>
              </v-col>
            </v-row>
          </div>
        </v-col>
         <MySkills />
      </v-row>
      <MyProjects />
    </v-container>
    <MyFooter />
  </v-app>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import MySkills from "./components/MySkills.vue";
import MyProjects from "./components/MyProjects.vue";
import MyFooter from "./components/MyFooter.vue";


export default {
  name: "App",
  data: () => ({
    icons: ["mdi-facebook", "mdi-twitter", "mdi-linkedin", "mdi-instagram"],
  }),
  components: {
    NavBar,
    MySkills,
    MyProjects,
    MyFooter,
  },
};
</script>
<style scoped>

.top {
  margin-top: 180px;
}
.topInverse {
  margin-top: -250px;
}
.topTolbar {
  margin-top: 100px;
  text-align: center;
}
.first {
  width: 100%;
  height: 610px;
  background: linear-gradient(
    to right,
    #181818,
    #181818 50%,
    #111111 50%,
    #111111 50%
  );
  text-align: center;
  margin-top: 4rem;
  padding: 2rem 2rem;
}

@media (min-width: 0px) and (max-width: 650px) {
        .first {
          height: 97rem;
        }
}


.second {
  width: 100%;
  height: 400px;
  background: #181818;
  text-align: center;
  padding: 2rem 2rem;
}
.secondchild1 {
  display: inline-block;
  background-color: #1e1e1e;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: left;
  margin-top: 250px;
}
.child {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: left;
  margin-right: 8px;
  width: 17.5rem;
}
.bgColor1 {
  background-color: #1e1e1e;
}
.bgColor2 {
  background-color: #ce1d2a;
}

.child1 {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  margin-right: 5px;
  width: 240px;
}
.child2 {
  display: inline-block;
  width: 245px;
  vertical-align: middle;
}
.mRight {
  margin-right: 8px;
}
.mButton {
  margin-bottom: 8px;
}
.padding {
  padding: 8px 0;
}

.col-12.padd {
  padding: 12px 0 !important;
}
.col-12.childcol {
  padding: 0 !important;
}
h1.number {
  font-size: 50px;
  font-weight: bold;
}
</style>