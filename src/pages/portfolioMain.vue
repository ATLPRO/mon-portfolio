<script setup>
import pageTitle from '@/components/pageTitle.vue';
import AboutMe from '@/components/AboutMe.vue';
import MesTechnos from '@/components/MesTechnos.vue';
import MesExperiences from '@/components/MesExperiences.vue';
import MesProjets from '@/components/MesProjets.vue';
import contactMe from '@/components/contactMe.vue';
import PageFooter from '@/components/PageFooter.vue';
</script>

<template>
  <div>
    <section id="accueil"> <pageTitle/></section>
   <section id="a-propos"><AboutMe/></section>
    
    <section id="mes-technos"><MesTechnos/></section> 
    <section id="experiences"><MesExperiences/></section>
    <section id="projets"><MesProjets/></section>
    <section id="contact"><contactMe/></section>
    <PageFooter/>
</div>
</template>

<style scoped>

</style>
