<template>
  <AppHeader :navbarCenterItems="navbarCenter" :navbarRightItems="navbarRight" />
</template>

<script>
import AppHeader from './components/AppHeader.vue'

export default {
  components: {
    AppHeader
  },
  data () {
    return {
      navbarCenter: [
        { type: 'link', text: 'HOME', href: '#', icon: '/public/svg/svg-0.svg' },
        { type: 'link', text: 'PAGES', href: '#' },
        { type: 'link', text: 'MENU', href: '#' },
        { type: 'image', src: '/public/img/logo.png', alt: 'Logo' },
        { type: 'link', text: 'EVENT', href: '#' },
        { type: 'link', text: 'BLOG', href: '#' },
        { type: 'link', text: 'LANDING', href: '#' }
      ],
      navbarRight: [
        { type: 'link', text: 'CART', href: '#', icon: '/public/svg/svg-1.svg' },
        { type: 'link', text: 'SEARCH', href: '#' }
      ]
    }
  }
}
</script>

<style scoped>
  
</style>
