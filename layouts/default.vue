<script>
import Header from './header.vue';
import MobileNavigation from '../components/MobileNavigation.vue';
import Footer from './footer.vue';
    export default{
    components: { Header, MobileNavigation, Footer },
    data(){
        return{
            mobileNavOpen:false
        }
    },
    methods:{
        toggleNavbar(){
            this.mobileNavOpen = !this.mobileNavOpen
        }
    }
}
</script>

<template>
    <div>
        <MobileNavigation :open="mobileNavOpen" @togglenavbar="toggleNavbar"/>
        <Header @togglenavbar="toggleNavbar"/>

        <Nuxt/>

        <Footer/>
        <nuxt-img class="fixed right-2 bottom-2 w-16 h-16 cursor-pointer" src="/whatsapp.png"/>
    </div>
</template>
