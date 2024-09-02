<template>
    <AdvertisingSection :images="AdvertisingImgs" />
    <TestimonialSection />
    <PizzaSpecials :pizzas="pizzaSpecials"/>
    <TeamSection />
    <ClientsSection  />
    <MenuPizza />
    <PizzaDeals />
</template>

<script>
import AdvertisingSection from './AdvertisingSection.vue';
import ClientsSection from './ClientsSection.vue';
import MenuPizza from './MenuPizza.vue';
import PizzaSpecials from './PizzaSpecials.vue';
import TeamSection from './TeamSection.vue';
import TestimonialSection from './TestimonialSection.vue';
import PizzaDeals from './PizzaDeals.vue';

export default {
    components: {
        AdvertisingSection,
        TestimonialSection,
        PizzaSpecials,
        TeamSection,
        ClientsSection,
        MenuPizza,
        PizzaDeals
    },
    data() {
        return {
            AdvertisingImgs: [
                {
                    src: '/public/img/h3-img-1.jpg',
                    clicked: false
                },
                {
                    src: '/public/img/h3-img-2.jpg',
                    clicked: false
                },
                {
                    src: '/public/img/h3-img-3.jpg',
                    clicked: false
                },
                {
                    src: '/public/img/h3-img-4.jpg',
                    clicked: false
                },
            ],
            pizzaSpecials: [
                {
                    prezzo: '$10',
                    nome: 'COMBO PICCOLO',
                    descrizione: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Praesent ut aliquam dui.'
                },
                {
                    prezzo: '$20',
                    nome: 'COMBO MEZZO',
                    descrizione: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Praesent ut aliquam dui.'
                },
                {
                    prezzo: '$30',
                    nome: 'COMBO GRANDE',
                    descrizione: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Praesent ut aliquam dui.'
                }
            ]
        }
    }
}
</script>

<style scoped>
    
</style>