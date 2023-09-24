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
