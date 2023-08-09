<template>
  <div class="main"><side-bar></side-bar> <MainLayout></MainLayout></div>
</template>

<script setup>
import MainLayout from "../views/MainLayout.vue";
import SideBar from "../views/SideBar.vue";
</script>

<style scoped lang="scss">
.main {
  display: flex;
  gap: 36px;
}
</style>
