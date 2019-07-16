<template>
    <header class="header">
        <div class="wrapper">
            <nav class="nav" v-if="Array.isArray(nav) && nav.length">
                <a class="nav__item" v-for="(link, index) in nav" :key="index" :href="link.href ? link.href : '#'">{{ link.title }}</a>
            </nav>
        </div>
    </header>
</template>

<script>
  export default {
    name: "HeaderTemplate",
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
    .nav
        display: flex
        justify-content: center
        flex-wrap: wrap
        &__item
            &:not(:last-child)
                margin-right: 20px
</style>