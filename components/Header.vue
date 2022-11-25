<template>
  <header class="flex items-center justify-between py-7 lg:px-desktop mx-auto">
    <NuxtLink to="/">
    <IconLogo/>
    </NuxtLink>

    <ul class="lg:flex hidden items-center space-x-14">
        <li :key="`navLink${i}`" v-for="(n, i ) in nav" >
            <NuxtLink :to="n.path" exact-active-class="border-primary border-b-2 pb-1"  class="font-medium hover:text-primary text-white transition-all duration-300">
                {{n.label}}
            </NuxtLink>
        </li>
    </ul>
    <!-- <img src="" alt=""> -->
  </header>
  
</template>

<script setup>
const nav = [
    {label:'Home',path:"/"},{label: "About Us",path:'/about'}, {label:"Services",path:'/services'}, {label:"Projects",path:'/project'}, {label:"Contact",path:'/contact'}
]
const activeLink = useState("activeLink", ()=> "Home");

</script>

