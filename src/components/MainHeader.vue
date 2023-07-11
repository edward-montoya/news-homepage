<template>
  <header class="header">
    <NavMenu :visible="visible" @close="close" />
    <div class="header__container">
      <img class="header__image" src="../assets/images/logo.svg" alt="application logo" />
      <button @click="open" class="header__menu">
        <img src="../assets/images/icon-menu.svg" alt="" />
      </button>
    </div>
  </header>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import NavMenu from '../components/NavMenu.vue';

const visible = ref(false);

function open() {
  visible.value = true;
}

function close() {
  visible.value = false;
}
</script>

<style lang="scss" scoped>
.header {
  &__container {
    display: flex;
    justify-content: space-between;
  }
  &__menu {
    &:hover {
      cursor: pointer;
    }
  }
}

@media screen and (min-width: 1024px) {
  .header {
    display: grid;
    grid-auto-flow: column;
    justify-content: space-between;
    direction: rtl;
    
    &__menu {
      display: none;
    }
    &__container {
      display: block;
      place-self: center;
    }
  }
}
</style>
