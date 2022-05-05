<template>
 <v-row>
  <v-col cols="12" sm="6" class="mt-16" >
    <v-card
      class="mx-auto mb-5 rounded-lg box-shadow"
      max-width="800"
      outlined
    >
      <v-list-item three-line>
        <v-list-item-content>
          <v-list-item-title class="text-h4 mb-1 font-weight-black">
            Wired Beauty
          </v-list-item-title>
          <div class="text-overline mb-4">Hackathon ·React · ChartJS</div>
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
  <v-col cols="12" sm="6" class="mt-16" >
    <v-card
      class="mx-auto mb-5 rounded-lg box-shadow"
      max-width="800"
      outlined
    >
      <v-list-item three-line>
        <v-list-item-content>
          <v-list-item-title class="text-h4 mb-1 font-weight-black">
            Expos3d
          </v-list-item-title>
          <div class="text-overline mb-4">Php · Js · Three.js</div>
          <div class="resume-card-text">Développement d'un site web permettant la génération automatique et semi-automatique d'une exposition virtuelle.</div>
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
</v-row>
    
</template>
<script>

import { Carousel, Slide } from 'vue-carousel';

/*
            <carousel-container>
            <styled-carousel>
              <slide v-for="(image, index) in buildSlideMarkup" :key="index">
                <carousel-image loading="lazy" v-bind:src="image['src']"/>
              </slide>
            </styled-carousel>
          </carousel-container>


*/

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
        src: 'wired/wired4.PNG',
        alt: 'Slide 3',
      },
      {
        src: 'wired/wired5.PNG',
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

.VueCarousel-pagination{
  position: absolute;
  bottom: 0;
}

.VueCarousel {
  max-width: 445px;
  cursor: grab;
}

.box-shadow{
  box-shadow: 6px 7px 10px #e1e1e152;
}

.image-card{
  margin: 1.5rem 0rem 1.5rem 1rem;
}

.card-project{
    width: 980px;
    background: radial-gradient(145% 145.46% at 0% 0%,#FFF 0%,#EEE 100%);
    box-shadow: 20px 20px 60px rgba(0,0,0,0.05),-20px -20px 60px rgba(255,255,255,0.8);
    border-radius: 20px;
    margin: auto;
    margin-bottom: auto;
  margin-bottom: 80px;
}

@media screen and (max-width: 530px) {
  .items {
    width: 100%;
    justify-content: center;
    align-content: center;
  }
}
</style>