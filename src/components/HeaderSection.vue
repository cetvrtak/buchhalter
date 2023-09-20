<template>
  <section class="header-section">
    <div class="main-container">
      <div class="header-container">
        <div class="header-logo-links-container">
          <div class="header-logo-container">
            <img
              src="../assets/logo.png"
              alt="Pascal Logo Image"
              class="header-logo"
            />
          </div>
          <ul class="header-links-container">
            <li class="header-link-container">
              <a href="#" class="header-link">Преимущества</a>
            </li>
            <li class="header-link-container">
              <a href="#" class="header-link">Услуги</a>
            </li>
            <li class="header-link-container">
              <a href="#" class="header-link">Новости</a>
            </li>
            <li class="header-link-container">
              <a href="#" class="header-link">Отзывы</a>
            </li>
          </ul>
        </div>
        <div class="header-contact-container">
          <div class="header-phone-container">
            <span class="header-phone">8 (812) 603-71-79</span>
          </div>
          <div class="header-button">
            <div class="header-button-text">Обратный звонок</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style>
.header-section {
  padding: 50px 0;
  background: #0a2641;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
}
.header-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.header-logo-links-container {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  gap: 48px;
}
.header-logo-container {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
}
.header-logo {
  margin-bottom: 5px;
}
.header-links-container {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 40px;
  list-style-type: none;
}
.header-link-container {
  display: flex;
  align-items: center;
  justify-content: center;
}
.header-link {
  transition: all 0.3s ease;
}
.header-link:link,
.header-link:visited {
  color: #fff;
  font-family: Inter;
  font-size: 15px;
  font-style: normal;
  font-weight: 600;
  line-height: 28px; /* 186.667% */

  opacity: 0.5;
  text-decoration: none;
}
.header-link:hover,
.header-link:active {
  opacity: 1;
}
.header-contact-container {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 24px;
}
.header-phone {
  color: #fff;
  font-family: Inter;
  font-size: 18px;
  font-style: normal;
  font-weight: 600;
  line-height: 28px; /* 155.556% */
}
.header-button {
  display: flex;
  width: 172px;
  height: 44px;
  padding: 10px 24px;
  align-items: flex-start;
  gap: 8px;
  flex-shrink: 0;

  border-radius: 32px;
  background: rgba(255, 255, 255, 0.15);
}
.header-button-text {
  color: #fff;
  font-family: Inter;
  font-size: 14px;
  font-style: normal;
  font-weight: 600;
  line-height: 24px; /* 171.429% */
}
</style>
