<script setup>
import { ref, onMounted, onBeforeUnmount } from "vue";
const time = ref(
  new Date().toLocaleTimeString([], { hour: "2-digit", minute: "2-digit" })
);

const updateClock = () => {
  time.value = new Date().toLocaleTimeString([], {
    hour: "2-digit",
    minute: "2-digit",
  });
};

const intervalId = setInterval(updateClock, 1000);

onMounted(() => {
  updateClock();
});

onBeforeUnmount(() => {
  clearInterval(intervalId);
});

const input = ref("");

const clearInput = () => {
  input.value = "";
};
</script>

<template>
  <div class="header-layout">
    <div class="header-left">
      <div class="logo">
        <img src="../assets/header-imgs/logo.svg" />
        <span>Логотип</span>
      </div>
      <button class="catalog-btn">Каталог</button>
    </div>
    <div class="header-search">
      <input
        type="text"
        class="search-bar"
        placeholder="Поиск по 100 000 товаров"
      />
    </div>
    <div class="header-right">
      <a href="" class="company-info"> Информация о компании </a>
      <a href="" class="contacts"> Контакты </a>
      <a href="" class="links"> Полезные ссылки </a>
    </div>
  </div>
  <div class="header-layout-mobile">
    <div class="header-mobile-top">
      <span class="time">{{ time }}</span>
      <div class="icons">
        <img src="../assets/header-mobile/connection.svg" alt="" />
        <img src="../assets/header-mobile/wi-fi.svg" alt="" />
        <img src="../assets/header-mobile/battery.svg" alt="" />
      </div>
    </div>
    <div class="header-mobile-bottom">
      <button class="arrow">
        <img src="../assets/header-mobile/arrow-img.svg" alt="" />
      </button>
      <input type="text" v-model="input" />
      <button id="remove-btn" v-if="input.length" @click="clearInput">
        <img src="../assets/header-mobile/remove-btn.svg" alt="" />
      </button>
      <button class="find">Найти</button>
    </div>
    <div class="line-after"></div>
  </div>
</template>

<style scoped lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@400;500&display=swap");

@media screen and (max-width: 1920px) {
  .header-layout-mobile {
    display: none;
  }
  .header-layout {
    font-family: "Inter", sans-serif;

    display: flex;
    padding: 12px 0px;
    align-items: center;
    align-self: stretch;
    gap: 24px;
    height: 48px;
    .header-left {
      display: flex;
      height: 100%;
      align-items: center;

      .logo {
        display: flex;
        height: 48px;
        padding: 0px 24px;
        align-items: center;
        gap: 8px;
        span {
          font-size: 16px;
          font-style: normal;
          font-weight: 400;
          line-height: normal;
        }
      }
      .catalog-btn {
        display: flex;
        height: 100%;
        padding: 8px 24px;
        align-items: center;
        gap: 10px;
        border-radius: 8px;
        border: 1px solid #73aff4;
        background: none;
        color: #000;
        font-family: Inter;
        font-size: 14px;
        font-style: normal;
        font-weight: 500;
        line-height: normal;
      }
      .catalog-btn:hover {
        background: #125bae;
        color: #00000060;
      }
    }
    .header-search {
      display: flex;
      width: 100%;
      height: 100%;

      .search-bar {
        display: flex;
        padding: 4px 16px;
        justify-content: center;
        align-items: center;
        gap: 8px;
        flex: 1 0 0;
        align-self: stretch;
        border-radius: 10px;
        border: 1px solid #73aff4;
      }
      .search-bar::placeholder {
        padding-left: 32px;
        color: #5a5a5a;
        font-family: Inter;
        font-size: 16px;
        font-style: normal;
        font-weight: 400;
        line-height: 150%;
        background: url("../assets/header-imgs/search-icon.svg") no-repeat;
      }

      .search-bar:focus {
        color: #2e2d2d;
        font-family: Inter;
        font-size: 16px;
        font-style: normal;
        font-weight: 400;
        line-height: 150%;
        border-color: #3aafdd;
        outline: 0;
        box-shadow: 0 0 0 0.1rem rgba(94, 146, 224, 0.418);
      }
      :focus::-webkit-input-placeholder {
        color: transparent;
        background: none;
      }
    }
    .header-right {
      display: flex;
      align-items: center;
      gap: 20px;
      height: 100%;
      * {
        white-space: nowrap;
        text-decoration: none;
        color: #393939;
        font-size: 14px;
        font-style: normal;
        font-weight: 400;
        line-height: normal;
      }
      *:hover {
        color: #3939398a;
      }
    }
  }
}

@media (max-width: 375px) {
  .header-layout {
    display: none;
  }

  .header-layout-mobile {
    display: flex;
    flex-direction: column;

    .header-mobile-top {
      display: flex;
      justify-content: space-between;
      padding: 0px 32px;
      align-items: center;
      height: 43px;
      .time {
        color: #333;
        text-align: justify;
        font-family: PT Sans;
        font-size: 14px;
        font-style: normal;
        font-weight: 400;
        line-height: normal;
      }
      .icons {
        display: flex;
        gap: 6px;
      }
    }
    .header-mobile-bottom {
      display: flex;
      align-items: center;
      padding: 8px 16px 0px 16px;

      gap: 10px;

      .arrow {
        border: none;
        background: none;
      }
      input {
        border: none;
        height: 100%;
      }
      input:focus {
        color: #333;
        border: none;
        font-family: PT Sans;
        font-size: 16px;
        font-style: normal;
        font-weight: 400;
        line-height: 14px;
      }

      #remove-btn {
        border: none;
        background: none;
      }
      .find {
        border: none;
        display: flex;
        padding: 12px 16px;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 10px;
        border-radius: 5px;
        background: #7397f5;
        color: #fff;
        font-family: PT Sans;
        font-size: 16px;
        font-style: normal;
        font-weight: 400;
        line-height: 14px;
      }
      .find:focus {
        background: #125bae;
      }
    }
    .line-after {
      margin-top: 8px;
      margin-right: 16px;
      width: 307px;
      height: 1px;
      background: #d5d5d5;
      align-self: flex-end;
    }
  }
}
</style>
