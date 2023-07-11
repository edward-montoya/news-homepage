<template>
  <article class="banner">
    <picture class="banner__picture">
      <source media="(min-width: 1024px)" srcset="../assets/images/image-web-3-desktop.jpg" />
      <img
        class="banner__image"
        src="../assets/images/image-web-3-mobile.jpg"
        alt="multiple blocks togetter"
      />
    </picture>
    <h1 class="banner__title">The Bright Future of Web 3.0?</h1>
    <p class="banner__description">
      We dive into the next evolution of the web that claims to put the power of the platforms back
      into the hands of the people. But is it really fulfilling its promise?
    </p>
    <div class="banner__button">
        <a
      href="/post/bright-future-web-3"
      aria-label="Read more about The Bright Future of Web 3.0? "
      class="banner__button"
      >read more</a
    >
    </div>
  </article>
</template>

<script setup lang="ts"></script>

<style lang="scss" scoped>
.banner {
  & > * {
    margin-top: 1rem;
  }
  &__picture {
    grid-area: picture;
  }
  &__image {
    width: 100%;
    box-sizing: border-box;
    margin-top: 2rem;
  }
  &__title {
    grid-area: title;
    font-weight: 800;
    font-size: 3rem;
  }
  &__description {
    grid-area: description;
    color: var(--vt-neutral-dark-gray);
    line-height: 1.4rem;
    margin-bottom: 3rem;
  }
  &__button {
    grid-area: button;
    color: white;
    text-transform: uppercase;
    letter-spacing: 0.4rem;
    & a {
        transition: all 200ms ease-in-out;
        &:hover, &:focus {
            background: black;
        }
        background-color: var(--vt-primary-soft-red);
        padding: 1rem 2rem;
    }
  }
}

@media screen and (min-width: 1024px) {
  .banner {
    display: grid;
    column-gap: 2rem;
    grid-template-areas: 'picture picture picture' 'picture picture picture' 'title description description' 'title button button';
    &__title {
      font-size: 3rem;
    }
    &__description {
        margin-bottom: 0;
    }
  }
}
</style>
