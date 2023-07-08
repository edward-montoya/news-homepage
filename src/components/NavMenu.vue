<template>
  <nav class="nav" :class="{ 'nav--visible': visible }">
    <div class="nav__container">
      <button @click="close" class="nav__close">
        <img src="../assets/images/icon-menu-close.svg" />
      </button>
      <ul class="nav__menu">
        <li><a href="/home" aria-label="Homepage">Home</a></li>
        <li><a href="/new" aria-label="New posts">New</a></li>
        <li><a href="/popular" aria-label="Popular posts">Popular</a></li>
        <li><a href="/treding" aria-label="Trending posts">Trending</a></li>
        <li><a href="/categories">Categories</a></li>
      </ul>
    </div>
  </nav>
</template>

<script setup lang="ts">
import { toRefs } from 'vue'

interface Input {
  visible: boolean
}

const props = defineProps<Input>()
const emit = defineEmits(['close'])
const { visible } = toRefs(props)

function close() {
  emit('close')
}
</script>

<style lang="scss" scoped>
.nav {
  position: fixed; /* Stay in place */
  z-index: 1; /* Sit on top */
  right: 0;
  top: 0;
  width: 0%; /* Full width */
  width: 100%; /* Full width */
  height: 100%; /* Full height */
  overflow: auto; /* Enable scroll if needed */
  visibility: hidden;
  background-color: rgb(0, 0, 0); /* Fallback color */
  background-color: rgba(0, 0, 0, 0.4); /* Black w/ opacity */
  $val: &;
  &--visible {
    visibility: initial;
    & > #{$val}__container {
        width: 70%;
    }
  }
  &__container {
    height: 100%;
    display: flex;
    flex-direction: column;
    box-sizing: border-box;
    width: 0%;
    margin-left: auto;
    background: white;
    padding: 2rem;
    transition: width 400ms ease-in;
  }
  &__menu {
    margin-top: 6rem;
    display: flex;
    flex-direction: column;
    gap: 2rem;
    & a {
        color: var(--vt-neutral-dark-gray);
    }
  }
  &__close {
    align-self: flex-end;
    z-index: 2; /* Sit on top */
  }
}

@media screen and (min-width: 1024px) {
  .nav {
    position: relative;
    visibility: inherit;
    background-color: white;
    overflow: hidden;
    padding: 0 0.2rem;
    &__container {
      display: flex;
      justify-content: center;
      width: 100%;
      padding: 0;
    }
    &__close {
      display: none;
    }
    &__menu {
      margin-top: 0;
      flex-direction: row-reverse;
      justify-items: center;
      align-items: center;
      font-size: 1.3rem;
      & a {
        color: var(--vt-neutral-dark-gray);
        transition: all 400ms ease-in-out;
        &:hover, &:focus {
          color: var(--vt-primary-soft-red);
        }
      }
    }
  }
  
}
</style>
