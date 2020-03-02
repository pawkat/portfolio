<template>
  <ul class="socials" v-if="Array.isArray(socials) && socials.length">
    <li class="socials__inner">
      <a class="socials__item" v-for="(link, index) in socials" :key="index" :href="link.href ? link.href : '#'"
         :title="link.title">
        <img :src="link.icon" :alt="link.title"/>
        <!--        <facebook></facebook>-->

      </a>
    </li>
  </ul>
</template>

<script>
  // import Facebook from "~assets/img/icons/facebook.svg?inline";

  export default {
    name: "Socials",
    comments: {
      // Facebook
    },
    data() {
      return {
        socials: [
          {
            title: 'Facebook',
            href: 'https://www.facebook.com/pashko.p',
            icon: require('~/assets/img/icons/facebook.svg'),
          },
          {
            title: 'Instagram',
            href: 'https://www.instagram.com/_pawkat_/',
            icon: require('~/assets/img/icons/instagram.svg'),
          }
        ]
      }
    }
  }
</script>

<style scoped lang="sass">
  .socials
    &__inner
      display: flex
      align-items: center

    &__item
      width: 1.75rem
      display: flex
      justify-content: center
      align-items: center
      &:not(:last-child)
        margin-right: 0.5rem

      img
        width: 100%
</style>
