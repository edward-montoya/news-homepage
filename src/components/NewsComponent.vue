<template>
    <section class="news">
        <h2 class="news__title news__title--main">New</h2>
        <ul class="news__container">
            <li>
                <article class="news__item">
                    <h3 class="news__title"><a href="/post/hydrogen-cs-electric/123232">Hydrogen VS Electric Cars</a></h3>
                    <p class="news__description">Will hidrogen-fueled cars ever catch up EV's?</p>
                </article>
            </li>
            <li>
                <article class="news__item">
                    <h3 class="news__title"><a href="/post/downsides-of-ia/325332">The Downsides of AI Artistry</a></h3>
                    <p class="news__description">What are the possible adverse effects of the on-demand AI image generation?</p>
                </article>
            </li>
            <li>
                <article class="news__item">
                    <h3 class="news__title"><a href="/post/is-vc-drying-up/45343">Is VC Funding Drying Up?</a></h3>
                    <p class="news__description">Private funding by VC firms is down 50% YOY. We take a look  at that means.</p>
                </article>
            </li>
        </ul>
    </section>
</template>

<script setup lang="ts">

</script>

<style lang="scss" scoped>
.news {
    background-color: var(--vt-neutral-dark-blue);
    padding: 1rem;
    margin-top: 4rem;
    &__container {
        display: flex;
        flex-direction: column;
        gap: 2rem;
        margin-top: 1rem;
    }
    &__title {
        margin: 0.6rem 0;
        font-weight: 700;
        font-size: 1.1rem;
        & > a {
            color: white;
            transition: all 400ms ease-in-out;
            &:hover {
                color: var(--vt-primary-soft-orange);
            }
            &:focus {
                color: var(--vt-primary-soft-orange);
                outline: 3px solid white;
            }
        }
        &--main {
            color: var(--vt-primary-soft-orange);
            font-size: 2rem;
        }
    }
    &__description {
        color: var(--vt-neutral-gray);
        margin-bottom: 30px;
        line-height: 1.4rem;
    }
    &__item {
        color: white;
        border-bottom: 1px solid var(--vt-neutral-gray);
        li:last-child > & {
            border-bottom: none;
        }
    }
}
@media screen and (min-width: 1024px) {
    .news {
        margin-top: 3rem;
    }
    
}
</style>