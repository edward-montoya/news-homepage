<template>
  <section class="top">
    <h2 class="sr-only">Top posts</h2>
    <ol class="top__list">
      <li class="top__item">
        <img class="top__image" src="../assets/images/image-retro-pcs.jpg" alt="Retro PCs image" />
        <h3 class="top__title">
          <a href="/posts/reviving-retro-pcs/346453">Reviving Retro PCs</a>
        </h3>
        <p class="top__description">What happens when old PCs are given modern upgrades?</p>
      </li>
      <li class="top__item">
        <img
          class="top__image"
          src="../assets/images/image-top-laptops.jpg"
          alt="Futuristic laptop"
        />
        <h3 class="top__title">
          <a href="/posts/top-10-laptos-2022/234232">Top 10 Laptops of 2022</a>
        </h3>
        <p class="top__description">Our best picks for various needs and budgets.</p>
      </li>
      <li class="top__item">
        <img class="top__image" src="../assets/images/image-gaming-growth.jpg" alt="Gamming PC" />
        <h3 class="top__title"><a href="/posts/grow-gaming/32424">The Grownth of Gaming</a></h3>
        <p class="top__description">How the pandemic has sparked fresh opportunities.</p>
      </li>
    </ol>
  </section>
</template>

<script setup lang="ts"></script>

<style lang="scss" scoped>
.top {
  margin-top: 4rem;
  &__list {
    list-style-type: decimal-leading-zero;
    list-style-position: inside;
    counter-reset: section;
  }
  &__item {
    display: grid;
    grid-template-areas:
      'image num num'
      'image title title'
      'image description description';
    column-gap: 1.4rem;
    margin-top: 2rem;
    &::before {
      counter-increment: section;
      content: counter(section, decimal-leading-zero);
      grid-area: num;
      font-weight: 900;
      color: var(--vt-neutral-gray);
      font-size: 2rem;
    }
  }
  &__image {
    grid-area: image;
    max-width: 6rem;
  }
  &__title {
    grid-area: title;
    font-weight: 700;
    & a {
      color: black;
      transition: all 200ms ease-in-out;
      &:hover,
      &:focus {
        color: var(--vt-primary-soft-red);
      }
    }
  }
  &__description {
    grid-area: description;
    color: var(--vt-neutral-dark-gray);
    line-height: 1.6rem;
  }
}

@media screen and (min-width: 1024px) {
  .top {
    &__list {
      display: flex;
    }
    &__item {
      margin-top: 0;
    }
  }
}
</style>
