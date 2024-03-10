<template>
    <HeaderComponent></HeaderComponent>
    <router-view />
    <FooterComponent></FooterComponent>
</template>

<script>
import FooterComponent from './components/FooterComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
export default {
  name: 'App',
    components: {
        HeaderComponent,
        FooterComponent
  },
  mounted() {
    window.scrollTo(0, 0);
  },
}
</script>

<style>
#app {
    margin:  0;  
    font-family: "Mulish", sans-serif;
    overflow-x: hidden;
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
}
</style>


