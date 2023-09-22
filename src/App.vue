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
