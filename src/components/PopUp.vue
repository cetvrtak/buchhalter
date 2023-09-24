<script>
import { useVuelidate } from '@vuelidate/core';
import { required, minLength, helpers } from '@vuelidate/validators';
import { mask } from 'vue-the-mask';

export default {
  setup() {
    return {
      v$: useVuelidate(),
    };
  },
  directives: { mask },
  data() {
    return {
      name: '',
      phone: '',
    };
  },
  validations() {
    return {
      name: {
        required: helpers.withMessage('Требуется значение.', required),
        minLenght: helpers.withMessage(
          'Это поле должно быть длиной не менее 3 символов.',
          minLength(3)
        ),
      },
      phone: { required: helpers.withMessage('Требуется значение.', required) },
    };
  },
};
</script>

<template>
  <div class="overlay"></div>
  <div class="popup-container">
    <div class="popup-close-btn">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="24"
        height="24"
        viewBox="0 0 24 24"
        fill="none"
      >
        <g opacity="0.4">
          <path
            d="M18 6L6 18M6 6L18 18"
            stroke="white"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
        </g>
      </svg>
    </div>
    <div class="popup-title-container">
      <span class="popup-title">Оставьте заявку и мы перезвоним</span>
    </div>
    <div class="popup-info-container">
      <div class="popup-input-container">
        <label for="name" class="popup-input-label">Имя</label>
        <input
          type="text"
          class="popup-input-field"
          id="name"
          placeholder="Иван"
          v-model="name"
        />
        <span class="popup-input-field-error-text" v-if="v$.name.$silentErrors">
          <template v-for="error in v$.name.$silentErrors" :key="error.$uid"
            >{{ error.$message }}&nbsp;
          </template>
        </span>
      </div>
      <div class="popup-input-container">
        <label for="phone" class="popup-input-label">Телефон</label>
        <input
          type="text"
          class="popup-input-field"
          id="phone"
          placeholder="+ 7"
          v-mask="'+7 (###) ###-##-##'"
          v-model="phone"
        />
        <span
          class="popup-input-field-error-text"
          v-if="v$.phone.$silentErrors"
        >
          <template v-for="error in v$.phone.$silentErrors" :key="error.$uid"
            >{{ error.$message }}&nbsp;
          </template>
        </span>
      </div>
    </div>
    <div class="popup-button-container">
      <div class="popup-button-desc">
        Нажимая на кнопку, я даю согласие на обработку персональных данных в
        соответствии с
        <span class="popup-button-desc-policy"
          >Политикой конфиденциальности</span
        >
      </div>
      <div class="popup-button">
        <div class="popup-button-text">Отправить</div>
      </div>
    </div>
  </div>
</template>

<style>
.overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.7);
  z-index: 999;
  display: none;
}
.popup-container {
  position: absolute;
  height: auto;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  display: none;
  z-index: 1000;

  border-radius: 32px;
  background: conic-gradient(
      from 212deg at 74.97% 23.7%,
      #ff6a2a 129.375deg,
      #4851fd 266.2499928474426deg
    ),
    linear-gradient(117deg, #4851fd 24.84%, #ff6a2a 124.17%), #4851fd;

  padding: 102px 119px 98px;
  width: 807px;
}
.popup-close-btn {
  width: 24px;
  height: 24px;
  flex-shrink: 0;

  opacity: 0.4;

  position: absolute;
  top: 32px;
  right: 32px;
}
.popup-title-container {
  margin-bottom: 74px;
}
.popup-title {
  color: #fff;
  font-family: Inter;
  font-size: 36px;
  font-style: normal;
  font-weight: 700;
  line-height: 48px; /* 133.333% */
}
.popup-info-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 34px;

  margin-bottom: 112px;
}
.popup-input-container {
  width: 100%;
  height: 96px;
  flex-shrink: 0;

  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
  gap: 8px;
}
.popup-input-label {
  color: #fff;
  font-family: Inter;
  font-size: 14px;
  font-style: normal;
  font-weight: 600;
  line-height: 28px; /* 200% */
  text-transform: uppercase;
}
.popup-input-field {
  width: 100%;
  height: 60px;
  flex-shrink: 0;

  border: none;
  border-radius: 32px;
  background: rgba(255, 255, 255, 0.1);

  padding: 16px 24px;
}
.popup-input-field,
.popup-input-field::placeholder,
.popup-input-field-error-text {
  color: #fff;
  font-family: Inter;
  font-size: 18px;
  font-style: normal;
  font-weight: 600;
  line-height: 28px; /* 155.556% */
}
.popup-input-field::placeholder {
  opacity: 0.5;
}
.popup-input-field-error-text {
  font-size: 12px;
  line-height: normal;
}
.popup-button-container {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 24px;
}
.popup-button-desc {
  color: #fff;
  font-family: Inter;
  font-size: 14px;
  font-style: normal;
  font-weight: 600;
  line-height: 20px; /* 142.857% */

  opacity: 0.5;
}
.popup-button-desc-policy {
  text-decoration: underline;
}
.popup-button {
  max-width: 162px;
  display: inline-flex;
  padding: 18px 32px;
  align-items: flex-start;
  justify-content: center;
  gap: 8px;

  border-radius: 32px 0px;
  background: #ff6a2a;
}
.popup-button-text {
  color: #fff;
  font-family: Inter;
  font-size: 18px;
  font-style: normal;
  font-weight: 600;
  line-height: 24px; /* 133.333% */
}

/* MEDIA QUERIES */
@media screen and (max-width: 1366px) {
  .popup-container {
    width: 647px;
    padding: 62px 39px 58px;
  }
}
@media screen and (max-width: 1024px) {
  .popup-container {
    width: 569px;
    padding: 62px 39px 58px;
  }
}
@media screen and (max-width: 650px) {
  .popup-container {
    width: 100%;
    min-height: 100vh;
    top: 0;
    left: 0;
    transform: translate(0, 0);
    padding: 72px 16px 48px;
    border-radius: initial;
  }
  .popup-close-btn {
    top: 16px;
    right: 16px;
  }
  .popup-title-container {
    width: 215px;
    margin: 0 auto 47px;
  }
  .popup-title {
    color: #fff;
    text-align: center;
    font-family: Inter;
    font-size: 24px;
    font-style: normal;
    font-weight: 700;
    line-height: 32px; /* 133.333% */
  }
  .popup-info-container {
    margin-bottom: 74px;
  }
  .popup-input-label {
    color: #fff;
    font-family: Inter;
    font-size: 9px;
    font-style: normal;
    font-weight: 600;
    line-height: 28px; /* 311.111% */
    text-transform: uppercase;
  }
  .popup-input-field {
    padding: 10px 12px 10px 16px;
  }
  .popup-input-field,
  .popup-input-field::placeholder {
    color: #fff;
    font-family: Inter;
    font-size: 12px;
    font-style: normal;
    font-weight: 600;
    line-height: 20px; /* 166.667% */
  }
  .popup-button-container {
    flex-direction: column;
    gap: 16px;
  }
  .popup-button-desc {
    color: #fff;
    text-align: center;
    font-family: Inter;
    font-size: 10px;
    font-style: normal;
    font-weight: 600;
    line-height: 16px; /* 160% */
  }
  .popup-button {
    max-width: none;
    width: 196px;
  }
}
</style>
