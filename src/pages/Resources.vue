<script setup lang="ts">
import { useHead } from '@unhead/vue';
import * as comms from '../committees.json'

useHead({
    title: 'Resources | GWH JMUN 2024'
})
</script>

<template>
    <main>
        <h1>Delegate Resouces</h1>
        <div class="bg">
            <div class="bg-link bg-matrix">
                <a href="#">
                    <h1>Country Matrix</h1>      
                </a>
                <p class="coming-soon">Coming Soon</p>
            </div>

            <div class="bg-link bg-code"> 
                <a href="/resources/code_of_conduct.pdf">
                    <h1>Code of Conduct</h1>
                </a>
            </div>
        </div>
        <h1>Background Guides</h1>        
        <div class="bg">
            <div class="bg-link" v-for="item in comms.list" :class="`bg-${item.id}`">
                <a :href="`/resources/${item.id}_bg.pdf`" v-if="item.na==false">
                    <h1>{{ item.id.toUpperCase() }}</h1>
                    <svg xmlns="http://www.w3.org/2000/svg" height="45" viewBox="0 -960 960 960" width="45"><path class="right-arrow" d="M647-440H160v-80h487L423-744l57-56 320 320-320 320-57-56 224-224Z"/></svg>
                </a>
                <div v-else class="invalid">
                    <h1>{{ item.id.toUpperCase() }} (TBD)</h1>
                </div>
            </div>
        </div>
    </main>
</template>

<style scoped>
.bg-link {
    display: flex;
    flex-direction: column; /* Stack children vertically */
    align-items: center; /* Center align text and items */
    text-align: center; /* Align text inside */
}

.coming-soon {
    margin-top: 8px; /* Add spacing between the title and the text */
    font-size: 1rem;
    color: gray;
}

main {
    padding: 10px;
}

main > h1 {
    text-align: center;
    font-size: 2.5em;
}

.bg {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

.bg-link {
    border: 2px solid #3b3b3b;
    border-radius: 20px;
    padding: 30px;
    margin: 15px;
    width: 200px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
}

.bg-link > a {
    text-decoration: none;
    color: #fff;
    display: flex;
    justify-content: center;
    align-items: center;
}

.bg-link h1 {
    font-size: 2em;
    text-align: center;
}

path.right-arrow {
    fill: #bbb;
}

.invalid {
    cursor: not-allowed;
}
</style>

<style>
.bg-matrix {
    background-image: url('/assets/bg_imgs/country_matrix.png');
}

.bg-code {
    background-image: url('/assets/bg_imgs/code_of_conduct.png');
}
</style>