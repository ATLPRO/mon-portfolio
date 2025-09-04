<script setup>
import portfolioMain from './pages/portfolioMain.vue';
import pageHeader from './components/pageHeader.vue';
</script>

<template>
  <header>
    <pageHeader/>
  </header>

  <main>
    <RouterView/>
  </main>
</template>

<style scoped>
header{
  width: 100%;
  line-height: 60px;
}
main{
  width: 100%;
}
</style>
