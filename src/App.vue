<template>
  <AppHeader :navbarCenterItems="navbarCenter" :navbarRightItems="navbarRight" />
  <AppMain />
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue';

export default {
  components: {
    AppHeader,
    AppMain
  },
  data () {
    return {
      navbarCenter: [
        { type: 'link', text: 'HOME', href: '#', icon: '/public/svg/svg-0.svg' },
        { type: 'link', text: 'PAGES', href: '#' },
        { type: 'link', text: 'MENU', href: '#' },
        { type: 'image', src: '/public/img/h5-logo-divided-header.png', alt: 'Logo' },
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
