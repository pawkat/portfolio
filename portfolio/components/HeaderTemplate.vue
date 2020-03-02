<template>
  <header class="header">
    <div class="wrapper">
      <div class="header__inner">
        <div class="header__nav">
          <nav class="nav" v-if="Array.isArray(nav) && nav.length">
            <a class="nav__item" v-for="(link, index) in nav" :key="index" :href="link.href ? link.href : '#'">{{
              link.title
              }}</a>
          </nav>
        </div>
        <div class="header__socials">
          <socials/>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
  import Socials from "./Socials";

  export default {
    name: "HeaderTemplate",
    components: {Socials},
    data() {
      return {
        nav: [
          {
            title: 'Home',
            href: '/'
          },
          {
            title: 'About',
          },
          {
            title: 'Contacts',
          },
        ]
      }
    }
  }
</script>

<style scoped lang="sass">
  .header
    background-color: $black
    padding: 1rem 0
    &__inner
      display: flex
      align-items: center

    &__socials
      margin-left: auto

    .nav
      display: flex
      align-items: center
      flex-wrap: wrap

      &__item
        color: $white

        &:hover
          color: $red

        &:not(:last-child)
          margin-right: 20px
</style>
