<template>
 <v-row>
  <h2 class="white--text2" id="section-projet">MES PROJETS</h2>
  <v-col cols="12" sm="12" class="mt-16" >
    <v-card
      class="mx-auto mb-5 rounded-lg box-shadow"
      max-width="850" padding-bottom="10"
      outlined
    >
      <v-list-item three-line>
        <v-list-item-content>
          <v-list-item-title class="text-h4 mb-1 font-weight-black">
            Wired Beauty
          </v-list-item-title>
          <div class="text-overline mb-4 style-project-skill">Hackathon ·React · ChartJS</div>
          <div class="resume-card-text">Mettre en place un site vitrine pour obtenir de nouveaux testeurs.</div>
          <div class="resume-card-text">Développer un dashboard permettant de rejoindre des campagnes ainsi que de récolter et afficher des statistiques.</div>
        </v-list-item-content>
          <v-carousel :perPage="1" :mouseDrag="true" :centerMode="true">
            <slide v-for="(image, index) in buildSlideMarkup" :key="index">
                    <v-img
          height="260"
          width="420"
          v-bind:src="image['src']"
          class="rounded-lg image-card"
        ></v-img>
            </slide>
          </v-carousel>

      </v-list-item>
    </v-card>
  </v-col>
  <v-col cols="12" sm="12" class="mt-16" >
    <v-card
      class="mx-auto mb-5 rounded-lg box-shadow"
      max-width="850"
      outlined
      padding-bottom="10"
    >
      <v-list-item three-line>
        <v-list-item-content>
          <v-list-item-title class="text-h4 mb-1 font-weight-black">
            Kindred
          </v-list-item-title>
          <div class="text-overline mb-4 style-project-skill">Symfony · React · ChartJS</div>
          <div class="resume-card-text">Développement d'un site web afin d'organiser la participation de vos enfants à la vie de la famille.</div>
          <div class="resume-card-text">Mise en place de l'interface avec React et création d'une api avec symfony</div>
        </v-list-item-content>

     
          <v-carousel :perPage="1" :mouseDrag="true" :centerMode="true">
            <slide v-for="(image, index) in buildSlideMarkupKindred" :key="index">
                    <v-img
          height="260"
          width="420"
          v-bind:src="image['src']"
          class="rounded-lg image-card"
        ></v-img>
            </slide>
          </v-carousel>

      </v-list-item>
    </v-card>
  </v-col>
  <v-col cols="12" sm="12" class="mt-16" >
    <v-card
      class="mx-auto mb-5 rounded-lg box-shadow"
      max-width="850"
      outlined
      padding-bottom="10"
    >
      <v-list-item three-line>
        <v-list-item-content>
          <v-list-item-title class="text-h4 mb-1 font-weight-black">
            Exposed
          </v-list-item-title>
          <div class="text-overline mb-4 style-project-skill">Php · Js · Three.js</div>
          <div class="resume-card-text">Développement d'un site web permettant la génération automatique d'une musée virtuelle.</div>
          <div class="resume-card-text">Le site permet notamment de générer un musée avec un fichier SVG mais également en dessinant sur une grille 2D</div>
        </v-list-item-content>

     
          <v-carousel :perPage="1" :mouseDrag="true" :centerMode="true">
            <slide v-for="(image, index) in buildSlideMarkupExposed" :key="index">
                    <v-img
          height="260"
          width="420"
          v-bind:src="image['src']"
          class="rounded-lg image-card"
        ></v-img>
            </slide>
          </v-carousel>

      </v-list-item>
    </v-card>
  </v-col>
</v-row>
    
</template>
<script>

import { Carousel, Slide } from 'vue-carousel';

export default {
  name: "FeaturedProjects",
  data: () => ({
    icons: ["mdi-facebook", "mdi-twitter", "mdi-linkedin", "mdi-instagram"],
    buildSlideMarkup : [
      {
        src: 'wired/wired1.PNG',
        alt: 'Slide 1',
      },
      {
        src: 'wired/wired2.PNG',
        alt: 'Slide 2',
      },
      {
        src: 'wired/wired3.PNG',
        alt: 'Slide 3',
      },
      {
        src: 'wired/wired6.PNG',
        alt: 'Slide 3',
      },
      {
        src: 'wired/wired7.PNG',
        alt: 'Slide 3',
      },
     ],
     buildSlideMarkupExposed : [
      {
        src: 'expos3d/expos3d.png',
        alt: 'Slide 1',
      },
     ],
     buildSlideMarkupKindred : [
      {
        src: 'kindred/image-1.png',
        alt: 'Slide 1',
      },
      {
        src: 'kindred/image-2.png',
        alt: 'Slide 1',
      },
      {
        src: 'kindred/image-3.png',
        alt: 'Slide 1',
      },
      {
        src: 'kindred/image-4.png',
        alt: 'Slide 1',
      },
     ]
  }),
  components: {
    'v-carousel' : Carousel,
    Slide,
  },
};
</script>
<style>

@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');


.v-image__image--cover{
  background-position: initial !important;
}
.style-project-skill{
  font-family: 'Poppins', sans-serif;
  font-weight: 600;
  font-size: 1.2rem;
  background-color: #1D2430;
  color: #fff;
  border-radius: 10px;
  text-align: center;
}
.white--text2{
  text-align: center;
  margin: auto;
  margin-top: 2em;
  color: white;
}
.VueCarousel-pagination{
  position: absolute;
  bottom: 0;
}

.VueCarousel {
  max-width: 445px;
  cursor: grab;
}

.v-list-item__content{
  padding: 15px 20px 15px 10px !important;
}

@media screen and (max-width: 800px) {
  .v-list-item {
    display: block !important;
  }
    .v-card{
    text-align: center;
  }

  .VueCarousel{
    margin: auto;
  }
}

.resume-card-test{
  font-family: "Poppins", sans-serif;
}

.theme--light.v-card {
  background-color: #FFFFFFD9 !important;
  color: rgba(0, 0, 0, 0.87);
  padding-bottom: 10px !important;
}

.box-shadow{
  box-shadow: 6px 7px 10px #97979752;
}

.image-card{
  margin: 1.5rem 0rem 1.5rem 1rem;
}

.card-project{
    width: 980px;
    background: #FFFC;
    background-color: #1D2430 !important;
    border-radius: 20px;
    margin: auto;
    margin-bottom: auto;
  margin-bottom: 80px;;
}

@media screen and (max-width: 530px) {
  .items {
    width: 100%;
    justify-content: center;
    align-content: center;
  }
}
</style>