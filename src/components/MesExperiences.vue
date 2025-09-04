<script setup>
import {ref} from 'vue';
let activeblock=ref(0)

let expériences=ref([{
    title:"Régal d'Afrik Scoops",
    date: " 2023",
    line1:" Stagiaire dans l'entreprise.",
    line2:" Gestionnaire des entrées sorties",
    line3:" Secretaire."   
},
{
    title:"Diesel Pump engeneering Co.LTD.",
    date: "2025",
    line1:" Conceptrice de site web.",
    line2:" Administration de la page facebook"
}
]);

const showXp=(id)=>{
    activeblock.value=id;
};


</script>

<template>
  <div id="xp">
    <h2 class="text-highlight-1 section-title"> Mes expériences</h2>
    <div id="left">
        <p :class="activeblock===0 ?'active':''" class="company fw600" @click="showXp(0)">Société n°1</p>
        <p :class="activeblock===1 ?'active':''" class="company fw600" @click="showXp(1)">Société n°2</p>      
    </div>
    <div id="right">
        <template v-for="(job,index) in expériences">
            <div class="job-details" :class="index===activeblock ? '':'hide'" :id="'block_'+index">
                <h3 class="fw600">{{ job.title }}</h3>
                <span id="date">{{ job.date }}</span>
                <br>
                <p class="fw600 mtb8" style="margin-top: 10px;"><span class="text-highlight-2"> *</span>{{ job.line1 }}</p>
                <p class="fw600 mtb8" style="margin-top: 10px;"><span class="text-highlight-2"> *</span>{{ job.line2 }}</p>
                <p class="fw600 mtb8" style="margin-top: 10px;"><span class="text-highlight-2"> *</span>{{ job.line3 }}</p>
            </div>
        </template>
    </div>
  </div>
</template>

<style scoped>
    #xp{
        margin-top: 40px;
    }
    #xp #left{
        float: left;
        width: 25%;
    }
    #xp #right{
        float: left;
        width: 75%;
    }
    #xp #right h3{
        font-size: 20px;
    }
    .fw600{
        font-weight: 600;
    }
    .mtb8{
        margin: 8px 0px;
    }
    #date{
        font-style: italic;
        font-size: 14px;
    }
    .company{
        border-left: 4px solid var(--vt-c-custom-text-1);
        line-height: 30px;
        padding-left: 10px;
    }
    .active{
        border-left: 4px solid var(--vt-c-custom-text-2);
        color: var(--vt-c-custom-text-2);
    }
    .company:hover{
        cursor: pointer;
        color: var(--vt-c-custom-text-1);
    }
    .hide{
        display: none;
    }
    @media screen and (max-width:600px) {
        #xp{
            margin-top: -240px;
        }
        #xp #right{
            width: 100%;
            margin-top: 20px;
        }
        #xp #left{
            width: 100%;
        }
        .company{
            border: none;
            padding-left: 0px;
            float: left;
            margin-left: 10px;
        }
    }
</style>
