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
          <div class="header-menu-links-container">
            <div class="header-menu-container">
              <div class="header-hamburger-wrapper">
                <svg
                  class="header-hamburger"
                  xmlns="http://www.w3.org/2000/svg"
                  width="20"
                  height="20"
                  viewBox="0 0 20 20"
                  fill="none"
                >
                  <path
                    d="M2.5 10H17.5M2.5 5H17.5M7.5 15H17.5"
                    stroke="#FF6A2A"
                    stroke-width="1.5"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  />
                </svg>
              </div>
              <div class="header-menu-icon-wrapper">
                <div class="header-menu-text">Меню</div>
                <svg
                  class="header-menu-icon"
                  xmlns="http://www.w3.org/2000/svg"
                  width="18"
                  height="18"
                  viewBox="0 0 18 18"
                  fill="none"
                >
                  <path
                    d="M4.5 6.75L9 11.25L13.5 6.75"
                    stroke="#FF6A2A"
                    stroke-width="2"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  />
                </svg>
              </div>
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
        </div>
        <div class="header-contact-container">
          <a href="tel:8 (812) 603-71-79" class="header-phone-container">
            <span class="header-phone">8 (812) 603-71-79</span>
          </a>
          <a href="tel:8 (812) 603-71-79" class="header-button">
            <div class="header-button-text">Обратный звонок</div>
          </a>
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
  z-index: 1;
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
.header-menu-icon-wrapper,
.header-hamburger-wrapper {
  display: none;
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
.header-phone-container {
  text-decoration: none;
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

  text-decoration: none;
}
.header-button-text {
  color: #fff;
  font-family: Inter;
  font-size: 14px;
  font-style: normal;
  font-weight: 600;
  line-height: 24px; /* 171.429% */
}

/* MEDIA QUERIES */
@media screen and (max-width: 1024px) {
  .header-section {
    padding: 30px 0;
  }
  .header-menu-icon-wrapper {
    display: inline-flex;
    align-items: center;
    gap: 4px;
    cursor: pointer;
  }
  .header-menu-text {
    color: #fff;
    font-family: Inter;
    font-size: 15px;
    font-style: normal;
    font-weight: 600;
    line-height: 24px; /* 160% */
  }
  .header-menu-icon {
    width: 18px;
    height: 18px;
  }
  .header-links-container {
    display: none;
    flex-direction: column;
    align-items: flex-start;
    gap: 0;
    position: absolute;
  }
  .header-links-container.active {
    display: flex;
  }
  .header-link-container {
    display: none;
  }
}
@media screen and (max-width: 767px) {
  .header-section {
    padding: 20px 0;
  }
  .header-container {
    position: relative;
    padding-right: 36px;
  }
  .header-menu-links-container {
    position: absolute;
    right: 0;
    top: 6px;
  }
  .header-links-container {
    right: 0;
    align-items: flex-end;
  }
  .header-menu-icon-wrapper,
  .header-button {
    display: none;
  }
  .header-hamburger-wrapper {
    display: flex;
  }
  .header-hamburger {
    width: 20px;
    height: 20px;
    flex-shrink: 0;
  }
}
@media screen and (max-width: 374px) {
  .header-section {
    padding: 16px 0;
  }
  .header-logo {
    content: url('../assets/logo_sm.png');
    margin: 0;
  }
  .header-phone {
    color: #fff;
    font-family: Inter;
    font-size: 13px;
    font-style: normal;
    font-weight: 600;
    line-height: 28px; /* 215.385% */
  }
  .header-menu-links-container {
    top: 4px;
  }
  .header-links-container.active {
    width: calc(100vw - 32px);
    margin-top: 6px;
  }
  .header-link-container {
    padding: 6px 0;
  }
}
</style>
