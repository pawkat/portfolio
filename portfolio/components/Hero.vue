<template>
    <div class="hero" style="background-image:url(/hero.jpg);">
        <div class="hero__top">
            <header-template></header-template>
        </div>
        <div class="hero__content">
            <div class="wrapper">
                <h1 class="title hero__title">
                    Portfolio site
                </h1>
            </div>
        </div>
        <div class="hero__bot">
            <div class="wrapper">
                <div class="hint hero__hint">
                    Nuxt.js project
                </div>
            </div>
        </div>

    </div>
</template>

<script>
  import HeaderTemplate from '~/components/HeaderTemplate.vue'

  export default {
    name: "Hero",
    components: {
      HeaderTemplate
    }
  }
</script>

<style scoped lang="sass">
    .hero
        min-height: 100vh
        display: flex
        flex-direction: column
        justify-content: space-between
        padding: 20px 0
        background-size: cover
        background-repeat: no-repeat
        background-position: center center

        &__title
            margin: 50px 0
            color: $white
            text-align: center
        &__bot
        &__hint
            text-align: right
</style>