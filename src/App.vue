<script setup>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
</script>

<template>
  <div class="layout">
    <Header></Header>
    <Main class="main"></Main>
  </div>
</template>

<style lang="scss" scoped>
.layout {
  display: flex;
  flex-direction: column;
  gap: 24px;
}

@media (max-width: 375px) {
  .layout {
    display: flex;
    width: 100%;
    height: 100%;
    gap: 12px;
    flex-direction: column;

    .main {
      display: flex;
      height: 800px;
      overflow: hidden;
    }
  }
}
</style>
