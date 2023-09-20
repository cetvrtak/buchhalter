<template>
  <PopUp />
  <HeaderSection />
  <HeroSection />
</template>

<script>
import HeroSection from './components/HeroSection.vue';
import PopUp from './components/PopUp.vue';
import HeaderSection from './components/HeaderSection.vue';
import $ from 'jquery';

$(document).ready(function () {
  const openPopUp = function () {
    $('.overlay, .popup-container').fadeIn('slow');
  };
  const closePopUp = function () {
    $('.overlay, .popup-container').hide();
  };

  $('.hero-button').on('click', openPopUp);
  $('.overlay, .popup-close-btn').on('click', closePopUp);
});

export default {
  name: 'App',
  components: {
    HeroSection,
    PopUp,
    HeaderSection,
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
