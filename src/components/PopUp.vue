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
  max-width: 569px;

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
</style>
