<script>
import BenefitsCard from '../components/BenefitCard.vue';

export default {
  data() {
    return {
      benefitsCards: [
        {
          id: 1,
          icon: 'calendar-check-02.svg',
          title: 'Сроки',
          desc: 'соблюдаем сроки сдачи отчетности и уплаты налогов',
        },
        {
          id: 2,
          icon: 'award-03.svg',
          title: 'Гарантии',
          desc: 'в случае ошибок возместим все штрафы и пени',
        },
        {
          id: 3,
          icon: 'shield-tick.svg',
          title: 'Конфиденциальность',
          desc: 'сохраним все ваши данные',
        },
        {
          id: 4,
          icon: 'route.svg',
          title: 'Удобно добираться',
          desc: 'находимся в центре города, у метро пл. Александра Невского',
        },
      ],
    };
  },
  components: {
    BenefitsCard,
  },
};
</script>

<template>
  <section class="benefits-section">
    <div class="main-container">
      <div class="benefits-container">
        <div class="benefits-title">Наши преимущества</div>
        <div class="benefits-cards-container">
          <template v-for="card in benefitsCards" :key="card.id">
            <benefitsCard
              :icon="require(`@/assets/${card.icon}`)"
              :title="card.title"
              :desc="card.desc"
            ></benefitsCard>
          </template>
        </div>
      </div>
    </div>
  </section>
  <img class="benefits-image" src="../assets/benefits-image.png" alt="" />
</template>

<style>
.benefits-section {
  background: #edf3f9;
}
.benefits-image {
  width: 100%;
  z-index: -1;
}
.benefits-container {
  padding-top: 80px;
  padding-bottom: 50px;
}
.benefits-title {
  margin-bottom: 48px;

  color: #0a2641;
  font-family: Inter;
  font-size: 36px;
  font-style: normal;
  font-weight: 700;
  line-height: 48px; /* 133.333% */
}
.benefits-cards-container {
  display: flex;
  align-items: flex-start;
  gap: 24px;
}

/* MEDIA QUERIES */
@media screen and (max-width: 1366px) {
  .benefits-cards-container {
    display: flex;
    align-items: flex-start;
    align-content: flex-start;
    gap: 24px;
    flex-wrap: wrap;
  }
}
@media screen and (max-width: 768px) {
  .benefits-container {
    padding-top: 56px;
  }
  .benefits-title {
    margin-bottom: 32px;
  }
}
@media screen and (max-width: 360px) {
  .benefits-container {
    padding-top: 32px;
  }
  .benefits-title {
    margin-bottom: 24px;

    color: #0a2641;
    font-family: Inter;
    font-size: 24px;
    font-style: normal;
    font-weight: 700;
    line-height: 32px; /* 133.333% */
  }
}
</style>
