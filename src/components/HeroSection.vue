<template>
  <section class="hero-section">
    <div class="main-container">
      <div class="hero-title-container">
        <p class="hero-title-bg">Бухгалтерские услуги в Санкт-Петербурге</p>
        <p class="hero-title-sm">Бухгалтерские услуги в СПБ</p>
      </div>
      <div class="hero-subtitle-container">
        <p class="hero-subtitle">
          Наши специалисты дадут исчерпывающую информацию по интересующим вас
          услугам
        </p>
      </div>
      <div class="hero-button">
        <span class="hero-button-text">Получить бесплатную консультацию</span>
      </div>
    </div>
  </section>
</template>

<style>
.hero-section {
  background: #0a2641;
  color: #fff;
  height: 100vh;

  display: flex;
  align-items: center;
  justify-content: center;
}
.hero-title-container {
  max-width: 807px;
  margin-bottom: 32px;
}
.hero-title-bg,
.hero-title-sm {
  color: #fff;
  font-family: Inter;
  font-size: 56px;
  font-style: normal;
  font-weight: 700;
  line-height: 72px; /* 128.571% */
}
.hero-title-sm {
  display: none;
}
.hero-subtitle-container {
  max-width: 451px;
  margin-bottom: 48px;
}
.hero-subtitle {
  color: #fff;
  font-family: Inter;
  font-size: 18px;
  font-style: normal;
  font-weight: 600;
  line-height: 28px; /* 155.556% */

  opacity: 0.5;
}
.hero-button {
  display: inline-flex;
  padding: 18px 32px;
  align-items: flex-start;
  gap: 8px;

  border-radius: 32px 0px;
  background: linear-gradient(117deg, #4851fd 24.84%, #ff6a2a 124.17%), #4851fd;

  cursor: pointer;
}
.hero-button-text {
  color: #fff;
  font-family: Inter;
  font-size: 18px;
  font-style: normal;
  font-weight: 600;
  line-height: 24px; /* 133.333% */
}

/* MEDIA QUERIES */
@media screen and (max-width: 768px) {
  .hero-section {
    align-items: flex-end;
  }
  .hero-title-bg {
    display: none;
  }
  .hero-title-sm {
    display: block;
  }
  .hero-button {
    margin-bottom: 98px;
  }
}
@media screen and (max-width: 500px) {
  .hero-title-container {
    max-width: none;
    width: 100%;
    margin-bottom: 24px;
  }
  .hero-title-bg,
  .hero-title-sm {
    color: #fff;
    font-family: Inter;
    font-size: 36px;
    font-style: normal;
    font-weight: 700;
    line-height: 48px; /* 133.333% */
  }
  .hero-subtitle-container {
    max-width: 288px;
    margin-bottom: 32px;
  }
  .hero-subtitle {
    color: #fff;
    font-family: Inter;
    font-size: 14px;
    font-style: normal;
    font-weight: 600;
    line-height: 22px; /* 157.143% */
  }
  .hero-button {
    display: flex;
    max-width: 288px;
    padding: 13px 16px;
    justify-content: center;
    align-items: center;
    gap: 8px;
  }
  .hero-button-text {
    color: #fff;
    font-family: Inter;
    font-size: 14px;
    font-style: normal;
    font-weight: 600;
    line-height: 22px; /* 157.143% */
    white-space: nowrap;
  }
}
@media screen and (max-width: 320px) {
  .hero-title-bg,
  .hero-title-sm {
    font-size: 30px;
    line-height: 32px;
  }
  .hero-button-text {
    font-size: 12px;
    line-height: 16px;
  }
}
</style>
