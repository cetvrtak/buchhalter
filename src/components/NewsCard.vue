<script>
export default {
  props: {
    img: String,
    desc: String,
    date: String,
  },
};
</script>

<template>
  <div class="news-card">
    <div class="news-image-container">
      <img :src="img" alt="" class="news-image" />
    </div>
    <div class="news-text">
      <div class="news-desc">
        {{ desc }}
      </div>
      <div class="news-date">{{ date }}</div>
    </div>
  </div>
</template>

<style>
.news-card {
  border-radius: 32px;
  background: #fff;
  box-shadow: 0px 5px 50px 0px rgba(0, 0, 0, 0.05);

  display: flex;
  flex-direction: column;
  align-items: flex-start;
  flex: 1 0 0;
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
