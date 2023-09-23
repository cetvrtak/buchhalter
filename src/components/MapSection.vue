<template>
  <div class="main-container">
    <div class="map-container" style="position: relative; overflow: hidden">
      <iframe
        class="map"
        src="https://yandex.ru/map-widget/v1/?ll=30.464414%2C59.864643&mode=whatshere&whatshere%5Bpoint%5D=30.464414%2C59.864643&whatshere%5Bzoom%5D=17&z=16"
        width="100%"
        height="472"
        allowfullscreen="true"
        style="position: relative"
      ></iframe>
    </div>
  </div>
</template>

<style>
.map-container {
  padding: 128px 0 72px;
}
.map {
  border: none;
  border-radius: 32px;
}

/* MEDIA QUERIES */
@media screen and (max-width: 768px) {
  .map-container {
    padding: 56px 0;
  }
}
@media screen and (max-width: 320px) {
  .map-container {
    padding: 40px 0;
  }
  .map {
    border-radius: 24px;
  }
}
</style>
