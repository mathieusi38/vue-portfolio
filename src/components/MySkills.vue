<template>
    <v-col cols="12" class="mt-16" >
    <div class="skill">
    <h2 class="white--text">MES COMPETENCES</h2>
    <div class="items mt-15">
    <div class="wrapper">
      <div class="icon logo">
        <div class="tooltip">
          HTML
        </div>
        <span><i class="fab fa-html5 fa-lg"></i></span>
      </div>
    </div>
    <div class="wrapper">
      <div class="icon logo">
        <div class="tooltip">
          CSS
        </div>
        <span><i class="fab fa-css3 fa-lg"></i></span>
      </div>
    </div>
    <div class="wrapper">
      <div class="icon logo">
        <div class="tooltip">
          Sass
        </div>
        <span><i class="fab fa-sass fa-lg"></i></span>
      </div>
    </div>
    <div class="wrapper">
      <div class="icon logo">
        <div class="tooltip">
          JavaScript
        </div>
        <span><i class="fab fa-js-square fa-lg"></i></span>
      </div>
    </div>
    <div class="wrapper">
      <div class="icon logo">
        <div class="tooltip">
          Php
        </div>
        <span><i class=" fab fa-php fa-lg"></i></span>
      </div>
    </div>
    <div class="wrapper">
      <div class="icon logo">
        <div class="tooltip">
          React.js
        </div>
        <span><i class="fab fa-react fa-lg"></i></span>
      </div>
    </div>
    </div>
    <div class="skill-button-wrapper mt-10 mb-15">
      <div class="skill-button">
        Référencement (SEO)
      </div>
      <div class="skill-button">
        UX & UI
      </div>
    </div>
  </div>
  </v-col>
</template>
<script>

export default {
  name: "MySkills",
  data: () => ({
    icons: ["mdi-facebook", "mdi-twitter", "mdi-linkedin", "mdi-instagram"],
  }),
  components: {
  },
};
</script>
<style scoped>


.skill-button{
  display: inline-flex;
  margin: auto;
  text-align: center;
  font-size: 12px;
-webkit-letter-spacing: 1.2px;
-moz-letter-spacing: 1.2px;
-ms-letter-spacing: 1.2px;
letter-spacing: 1.2px;
padding: 2px 14px;
font-weight: bold;
margin-right: 20px;
border-radius: 24px;
line-height: 40px;
color: #222;
background: #fafafa;
margin-top: 1rem;
}
.skill{
  text-align: center;
}
.fab{
color: white;
}
h1 {
  font-weight: 500;
  color: white;
  font-size: 1.8rem;
  border-bottom: 10px solid green;
  line-height: 0.4;
  width: 80px;
  transition: all ease 0.3s;
}
h1:hover {
  font-size: 1.8rem;
  font-weight: 500;
  color: white;
  border-bottom: 10px solid #1DB954;
  line-height: 0.4;
  width: 130px;
  transition: 0.5s;
}
span {
  padding: 20px;
}
.wrapper {
  display: inline-flex;
  vertical-align: center;
}
.wrapper .icon {
  margin: 0 10px;
  text-align: center;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  position: relative;
  z-index: 2;
  transition: 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
}
.wrapper .icon span {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 60px;
  width: 60px;
  margin-bottom: 1em;
  background-color: #1D2430;
  border-radius: 50%;
  position: relative;
  z-index: 2;
  box-shadow: 0px 10px 10px rgba(0, 0, 0, 0.1);
  transition: 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
}
.wrapper .icon span i {
  line-height: 60px;
  font-size: 25px;
}
.wrapper .icon .tooltip {
  position: absolute;
  top: 0;
  z-index: 1;
  background: #fff;
  color: #fff;
  padding: 5px 15px;
  font-size: 17px;
  font-weight: 500;
  border-radius: 25px;
  opacity: 0;
  pointer-events: none;
  box-shadow: 0px 10px 10px rgba(0, 0, 0, 0.1);
  transition: 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
}
.wrapper .icon:hover .tooltip {
  top: -50px;
  opacity: 1;
  pointer-events: auto;
}
.fa-python {
  color: #fff;
}
.fa-react {
  color: #fff;
}
.fa-sass {
  color: #fff;
}
.fa-vuejs {
  color: #fff;
}
.fa-node-js {
  color: #fff;
}
.fa-html5 {
  color: #fff;
}
.fa-css3 {
  color: #fff;
}
.fa-js-square {
  color: #fff;
}
.icon .tooltip:before {
  position: absolute;
  content: "";
  height: 15px;
  width: 15px;
  background: #fff;
  left: 50%;
  bottom: -6px;
  transform: translateX(-50%) rotate(45deg);
  transition: 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
}
.wrapper .icon:hover span {
  color: #fff;
}
.wrapper .icon:hover span,
.wrapper .icon:hover .tooltip {
  text-shadow: 0px -1px 0px rgba(255, 255, 255, 0.5);
}
.wrapper .logo:hover span,
.wrapper .logo:hover .tooltip,
.wrapper .logo:hover .tooltip:before {
  background: #B71C1C;
}
.items {
  margin: auto 0;
  align-content: center !important;
  justify-content: center;
}
@media screen and (max-width: 530px) {
  .items {
    width: 100%;
    justify-content: center;
    align-content: center;
  }
}
</style>