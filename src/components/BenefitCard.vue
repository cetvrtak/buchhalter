<script>
export default {
  props: {
    icon: String,
    title: String,
    desc: String,
  },
};
</script>

<template>
  <div class="benefits-card-container">
    <div class="benefits-card-icon-container">
      <img :src="icon" alt="" class="benefits-card-icon" />
    </div>
    <div class="benefits-card-text-container">
      <span class="benefits-card-title">{{ title }}</span>
      <span class="benefits-card-desc">{{ desc }}</span>
    </div>
  </div>
</template>

<style>
.benefits-card-container {
  display: flex;
  padding: 32px;
  flex-direction: column;
  align-items: flex-start;
  gap: 24px;
  flex: 1 0 0;
  align-self: stretch;

  border-radius: 32px;
  background: #4851fd;

  min-width: 311.5px;
}
.benefits-card-icon-container {
  width: 64px;
  height: 64px;
  background: #ffffff;
  border-radius: 50%;

  display: flex;
  align-items: center;
  justify-content: center;
}
.benefits-card-icon {
  width: 32px;
  height: 32px;
}
.benefits-card-text-container {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 8px;
  align-self: stretch;
}
.benefits-card-title {
  align-self: stretch;

  color: #fff;
  font-family: Inter;
  font-size: 20px;
  font-style: normal;
  font-weight: 600;
  line-height: 32px; /* 160% */
}
.benefits-card-desc {
  align-self: stretch;

  color: #fff;
  font-family: Inter;
  font-size: 16px;
  font-style: normal;
  font-weight: 600;
  line-height: 24px; /* 150% */

  opacity: 0.8;
}

/* MEDIA QUERIES */
@media screen and (max-width: 694px) {
  .benefits-card-container {
    min-width: 288px;
  }
}
@media screen and (max-width: 360px) {
  .benefits-card-container {
    display: flex;
    padding: 24px;
    flex-direction: column;
    align-items: flex-start;
    gap: 8px;

    border-radius: 24px;
    background: #4851fd;
  }
  .benefits-card-icon-container {
    width: 48px;
    height: 48px;
  }
  .benefits-card-icon {
    width: 24px;
    height: 24px;
  }
  .benefits-card-text-container {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 4px;
    align-self: stretch;
  }
  .benefits-card-title {
    color: #fff;
    font-family: Inter;
    font-size: 18px;
    font-style: normal;
    font-weight: 600;
    line-height: 32px; /* 177.778% */
  }
  .benefits-card-desc {
    color: #fff;
    font-family: Inter;
    font-size: 16px;
    font-style: normal;
    font-weight: 600;
    line-height: 24px; /* 150% */
  }
}
@media screen and (max-width: 320px) {
  .benefits-card-container {
    min-width: auto;
  }
}
</style>
