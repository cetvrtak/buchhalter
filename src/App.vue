<template>
  <PopUp />
  <HeaderSection />
  <HeroSection />
  <BenefitsSection />
  <div class="main-container">
    <NewsSection />
    <MapSection />
  </div>
</template>

<script>
import HeroSection from './components/HeroSection.vue';
import PopUp from './components/PopUp.vue';
import HeaderSection from './components/HeaderSection.vue';
import BenefitsSection from './components/BenefitsSection.vue';
import NewsSection from './components/NewsSection.vue';
import MapSection from './components/MapSection.vue';
import $ from 'jquery';

$(document).ready(function () {
  $('.header-menu-container').on('click', function () {
    $('.header-links-container, .header-link-container').toggleClass('active');

    var $headerLinksContainer = $('.header-links-container');

    function openLinks() {
      var $links = $headerLinksContainer.find('li');

      var currentIndex = 0;

      // Function to open links one by one
      function animateLink() {
        if (currentIndex < $links.length) {
          // Display the current link with a slide-down animation
          $($links[currentIndex]).slideDown('slow', function () {
            // Increment the index and call the function recursively
            currentIndex++;
            animateLink();
          });
        }
      }

      // Call the function to start opening links
      animateLink();
    }

    if ($headerLinksContainer.hasClass('active')) {
      // Call the openLinks function here when needed
      openLinks();
    } else {
      // If the container is not active (links are hidden), hide all links
      $headerLinksContainer.find('li').hide();
    }
  });
});

export default {
  name: 'App',
  components: {
    HeroSection,
    PopUp,
    HeaderSection,
    BenefitsSection,
    NewsSection,
    MapSection,
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
  width: 100%;
}
.main-container {
  max-width: 1400px;
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
