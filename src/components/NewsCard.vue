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
  <a href="#" class="news-card">
    <div class="news-image-container">
      <img :src="img" alt="" class="news-image" />
    </div>
    <div class="news-text">
      <div class="news-desc">
        {{ desc }}
      </div>
      <div class="news-date">{{ date }}</div>
    </div>
  </a>
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

  text-decoration: none;
  transition: all 0.3s;
}
.news-card:hover {
  transform: scale(1.03);
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

/* MEDIA QUERIES */
@media screen and (max-width: 320px) {
  .news-card {
    border-radius: 24px;
    background: #fff;
    box-shadow: 0px 5px 50px 0px rgba(0, 0, 0, 0.05);
  }
  .news-image {
    border-radius: 24px 24px 0px 0px;
  }
  .news-text {
    display: flex;
    padding: 16px;
    flex-direction: column;
    align-items: flex-start;
    gap: 16px;
    align-self: stretch;
  }
  .news-desc {
    color: #0a2641;
    font-family: Inter;
    font-size: 16px;
    font-style: normal;
    font-weight: 600;
    line-height: 24px; /* 150% */
  }
  .news-date {
    color: #5f83a7;
    font-family: Inter;
    font-size: 12px;
    font-style: normal;
    font-weight: 600;
    line-height: 20px; /* 166.667% */
  }
}
</style>
