<script setup lang="ts">
import { ref, watch } from "vue";
import { useRoute } from "vue-router";

const width = ref(window.innerWidth)
const mobile_menu_shown = ref(false)
window.addEventListener("resize", () => {
    width.value = window.innerWidth
})

const route = useRoute()
watch(
  () => route.fullPath,
  async () => {
    mobile_menu_shown.value = false
  }
)
</script>

<template>
    <header class="navbar">
        <div class="desktop-nav" v-if="width>450">
            <ul class="links">    
                <li><RouterLink to="/"><img src="/assets/gwhmun_logo.png" class="navbar-logo"></RouterLink></li>
                <li><RouterLink to="/">Home</RouterLink></li>
                <!--<li><RouterLink to="/team">Team</RouterLink></li>-->
                <li><RouterLink to="/committees">Committees</RouterLink></li>
                <li><RouterLink to="/resources">Resources</RouterLink></li>
                <li><RouterLink to="/registrations">Registrations</RouterLink></li>
                <li></li>
            </ul>
        </div>
        <div class="mobile-nav" v-else>
            <RouterLink to="/"><img src="/assets/gwhmun_logo.png" class="navbar-logo"></RouterLink>
            <button class="nav-show" @click="mobile_menu_shown=true"><svg xmlns="http://www.w3.org/2000/svg" height="24" viewBox="0 -960 960 960" width="24"><path d="M120-240v-80h720v80H120Zm0-200v-80h720v80H120Zm0-200v-80h720v80H120Z"/></svg></button>
        </div>
    </header>
    <div class="mobile-menu" v-if="mobile_menu_shown">
            <ul class="links">
                <li><button class="nav-hide" @click="mobile_menu_shown=false"><svg xmlns="http://www.w3.org/2000/svg" height="24" viewBox="0 -960 960 960" width="24"><path d="m256-200-56-56 224-224-224-224 56-56 224 224 224-224 56 56-224 224 224 224-56 56-224-224-224 224Z"/></svg></button></li>
                <li><RouterLink to="/">Home</RouterLink></li>
                <li><RouterLink to="/committees">Committees</RouterLink></li>
                <li><RouterLink to="/resources">Resources</RouterLink></li>
                <li><RouterLink to="/registrations">
                    <b>Registrations</b>
                </RouterLink></li>
            </ul>
        </div>
    <RouterView/>
    <footer>
        <img src="/assets/gwhmun_logo.png" class="footer-logo">
        <div class="footer-info">
            <h3 class="subhead">Location</h3>
            <div><a href="https://www.google.com/maps/place/Greenwood+High+-+Sarjapur/@12.8995914,77.7464884,17z/data=!3m1!4b1!4m6!3m5!1s0x3bae0d59425e7257:0xb036140cfb4656dd!8m2!3d12.8995862!4d77.7490633!16s%2Fm%2F0wbm4qb?entry=tts&shorturl=1">Greenwood High School Sarjapur</a></div>
        </div>
        <div class="footer-info">
            <h3 class="subhead"> Contact</h3>
            <div>Secretary General - <a href="mailto:amisha.sharma.27102008@gmail.com">Amisha Sharma</a></div>
            <div>Director General - <a href="mailto:varun070052@greenwoodhigh.edu.in">Varun Iyer</a></div>
        </div>
    </footer>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Raleway:wght@400;700&display=swap');

body {
    font-family: 'Raleway', sans-serif !important;
    background-color: #1a1a1a;
    color: #fff;
}

header.navbar {
    height: 60px;
    background-color: #1a1a1a;
    position: sticky;
    top: 0;
    padding: 10px
}

.desktop-nav {  
    display: flex;
    flex-direction: row;
}

.mobile-nav {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
}

.navbar-logo {
    height: 45px;
    width: auto;
}

.mobile-menu {
    position: fixed;
    top:0;
    left:0;
    background-color: #1a1a1a;
    height: 100vh;
    width: 100vw;
}

ul.links {
    list-style: none;
    padding: 0;
    margin: 0;
    font-size: 1.2em;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    width: 100%;
}

ul.links li {
    padding: 10px 0;
    display: inline;
    font-weight: bold;
    font-size: 1.25em;
}

ul.links li a {
    color: #fff;
    text-decoration: none;
}

ul.links li a:hover {
    color: #b4d0d4;
}

.mobile-menu > ul.links {
    margin: 100px 50px;
    text-align: center;
    display: flex;
    flex-direction: column;
    font-size: 1.6em;
}

button.nav-show, button.nav-hide {
    background-color: #1a1a1a;
    border: 0px
}

button.nav-show path, button.nav-hide path {
    fill: #fff;
}

footer {
    border-top: 2px solid #3b3b3b;
    padding: 15px 0;
    display: flex;
    align-items: center;
    flex-direction: column;
}

img.footer-logo {
    height: 100px;
    width: auto;
}

.footer-info {
    margin: 10px;
    text-align: center;
}

.footer-info > h3 {
    margin: 5px;
}

footer a {
    text-decoration: none;
    color: #b4d0d4;
}
</style>