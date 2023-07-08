<template>
    <section class="top">
        <article class="top__container">
            <img class="top__image" src="../assets/images/image-retro-pcs.jpg" />
            <span class="top__numeration">01</span>
            <h3 class="top__title">Reviving Retro PCs</h3>
            <p class="top__description">What happens when old PCs are given modern upgrades?</p>
        </article>
        <article class="top__container">
            <img class="top__image" src="../assets/images/image-top-laptops.jpg" />
            <span class="top__numeration">02</span>
            <h3 class="top__title">Top 10 Laptops of 2022</h3>
            <p class="top__description">Our best picks for various needs and budgets.</p>
        </article>
        <article class="top__container">
            <img class="top__image" src="../assets/images/image-gaming-growth.jpg" />
            <span class="top__numeration">03</span>
            <h3 class="top__title">The Grownth of Gaming</h3>
            <p class="top__description">How the pandemic has sparked fresh opportunities.</p>
        </article>
    </section>
</template>

<script setup lang="ts">

</script>

<style lang="scss" scoped>
.top {
    margin-top: 4rem;
    &__container {
        display: grid;
        grid-template-areas: 'image num num'
                             'image title title'
                             'image description description';
        column-gap: 1.4rem;
        margin-top: 2rem;
    }
    &__image{
        grid-area: image;
        max-width: 6rem;
    }
    &__numeration {
        grid-area: num;
        font-weight: 900;
        color: var(--vt-neutral-gray);
        font-size: 2rem;
    }
    &__title {
        grid-area: title;
        font-weight: 700;
    }
    &__description {
        grid-area: description;
        color: var(--vt-neutral-dark-gray);
        line-height: 1.6rem;
    }
}

@media screen and (min-width: 1024px) {
    .top {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 2rem;
        &__image{
            max-width: 10rem;
        }
    }
}
</style>