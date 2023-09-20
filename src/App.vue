<template>
  <PopUp />
  <HeroSection />
</template>

<script>
import HeroSection from './components/HeroSection.vue';
import PopUp from './components/PopUp.vue';
import $ from 'jquery';

$(document).ready(function () {
  const openPopUp = function () {
    $('.overlay').show();
  };
  const closePopUp = function () {
    $('.overlay').hide();
  };

  $('.hero-button').on('click', openPopUp);
  $('.overlay').on('click', closePopUp);
});

export default {
  name: 'App',
  components: {
    HeroSection,
    PopUp,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  font-family: Inter;
}
.main-container {
  max-width: 1440px;
  width: 100%;
  margin: 0 auto;
}

/* MEDIA QUERIES */
@media screen and (max-width: 1440px) {
  .main-container {
    padding: 0 24px;
  }
}
@media screen and (max-width: 320px) {
  .main-container {
    padding: 0 16px;
  }
}
</style>
