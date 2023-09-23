<script>
import 'slick-carousel/slick/slick.min.js';
import 'slick-carousel/slick/slick.css';
import 'slick-carousel/slick/slick-theme.css';
import $ from 'jquery';

export default {
  mounted() {
    $(this.$refs.slickCarousel).slick({
      infinite: true,
      slidesToShow: 3,
      slidesToScroll: 1,
      dots: true,
    });
  },
};
</script>

<template>
  <section class="news-section">
    <div class="news-container">
      <div class="news-title">Новости</div>
      <div class="news-carousel" ref="slickCarousel">
        <div class="news-card">
          <div class="news-image-container">
            <img src="../assets/news-image-1.png" alt="" class="news-image" />
          </div>
          <div class="news-text">
            <div class="news-desc">
              Критерии упрощенной системы налогообложения в 2023 году
            </div>
            <div class="news-date">29 мая 2023</div>
          </div>
        </div>
        <div class="news-card">
          <div class="news-image-container">
            <img src="../assets/news-image-2.png" alt="" class="news-image" />
          </div>
          <div class="news-text">
            <div class="news-desc">
              Критерии упрощенной системы налогообложения в 2023 году
            </div>
            <div class="news-date">29 мая 2023</div>
          </div>
        </div>
        <div class="news-card">
          <div class="news-image-container">
            <img src="../assets/news-image-3.png" alt="" class="news-image" />
          </div>
          <div class="news-text">
            <div class="news-desc">
              Критерии упрощенной системы налогообложения в 2023 году
            </div>
            <div class="news-date">29 мая 2023</div>
          </div>
        </div>
        <div class="news-card">
          <div class="news-image-container">
            <img
              src="https://picsum.photos/451/297"
              alt=""
              class="news-image"
            />
          </div>
          <div class="news-text">
            <div class="news-desc">
              Критерии упрощенной системы налогообложения в 2023 году
            </div>
            <div class="news-date">29 мая 2023</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style>
.news-section {
  padding: 120px 0;
}
.news-title {
  color: #0a2641;
  font-family: Inter;
  font-size: 36px;
  font-style: normal;
  font-weight: 700;
  line-height: 48px; /* 133.333% */

  margin-bottom: 40px;
}
.slick-track {
  display: flex;
  gap: 24px;
}
.news-card {
  border-radius: 32px;
  background: #fff;
  box-shadow: 0px 5px 50px 0px rgba(0, 0, 0, 0.05);

  display: flex;
  flex-direction: column;
  align-items: flex-start;
  flex: 1 0 0;
}
.news-image {
  border-radius: 32px 32px 0px 0px;
  width: 100%;
}
.news-text {
  display: flex;
  padding: 24px;
  flex-direction: column;
  align-items: flex-start;
  gap: 24px;
  align-self: stretch;
}
.news-desc {
  align-self: stretch;

  color: #0a2641;
  font-family: Inter;
  font-size: 20px;
  font-style: normal;
  font-weight: 600;
  line-height: 28px; /* 140% */
}
.news-date {
  align-self: stretch;

  color: #5f83a7;
  font-family: Inter;
  font-size: 16px;
  font-style: normal;
  font-weight: 600;
  line-height: 24px; /* 150% */
}
</style>
