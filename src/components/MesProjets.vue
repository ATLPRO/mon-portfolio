<script setup>
import {ref} from 'vue';
import ProjetSingle from './ProjetSingle.vue';
let projects=ref([{
    name:"Application de gestion de stock et de production",
    image: "accueil1.PNG",
    tags:" VueJs;API Rest PHP",
    description:" Ceci a permi de resoudre le probleme de rupture de stock et de suivi des couts de production",
    tasks:" Permet de decider rapidement sur une nouvelle production."
},
{
    name:"Site web pour diesel pump",
    image: "projet1.jpg",
    tags:"Bootstrap;HTML;CSS;JS",
    description:"Dans le but de se faire connaitre, de partager ses produits et services et d'attirrer le maximum de clients.",
    tasks:" Responsive."   
}
]);

</script>

<template>
  <div  id="projets">
    <h2 class="text-highlight-1 section-title"> Quelques Projets</h2>
    <ProjetSingle v-for="(project,index) in projects" :key="project.name" :project="project" :reverse="index % 2==0 ? false : true "/>
  </div>
    
</template>

<style scoped>
#projets{
  display: inline-block;
  margin-top: 40px;
}
</style>