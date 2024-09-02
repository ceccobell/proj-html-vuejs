<template>
  <AppHeader :navbarCenterItems="navbarCenter" :navbarRightItems="navbarRight" />
  <AppMain />
  <AppFooter :ourRestaurants="ourRestaurants" :workingHours="workingHours"/>
</template>

<script>
import AppFooter from './components/AppFooter.vue';
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue';

export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter
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
      ],
      ourRestaurants: [
        {
          via: '1614 E. Bell Rd #104.',
          city: 'Salerno, AZ 85022',
          telefono: '(602) 867-1010'
        },
        {
          via: '204 E. Pizzetta Tommaso',
          city: 'Sorrento, AZ 85022',
          telefono: '(358) 867-1010'
        },
        {
          via: 'Viale Puglia 54',
          city: 'Torre Del Greco, AZ 85022',
          telefono: '(359) 867-1010'
        },
        {
          via: 'Corso Italia',
          city: 'Naples, AZ 85022',
          telefono: '(989) 867-1010'
        },
      ],
      workingHours: [
        {
          day: 'MONDAY',
          openingHours: 'Kitchen Closed'
        },
        {
          day: 'TUESDAY UNTIL FRIDAY',
          openingHours: '9:00 - 22:00'
        },
        {
          day: 'SATURDAY',
          openingHours: 'Saturday 11am to midnight'
        },
        {
          day: 'SUNDAY',
          openingHours: '9:00 - 22:00'
        },
      ]
    }
  }
}
</script>

<style scoped>
  
</style>
