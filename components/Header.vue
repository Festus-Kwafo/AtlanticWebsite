<template>
  <header class="flex items-center justify-between py-7 lg:px-desktop mx-auto">
    <NuxtLink to="/">
    <IconLogo/>
    </NuxtLink>

    <ul class="lg:flex hidden items-center space-x-14">
        <li class="group text-[white]" :key="`navLink${i}`" v-for="(n, i ) in nav" >
            <NuxtLink to="#" class="font-medium group-hover:text-white transition-all duration-300">
                {{n}}
            </NuxtLink>
            <div :class="{'bg-[#E9500E] scale-y-100': activeLink== n}" class="h-0.5 mt-0.5 group-hover:bg-primary group-hover:block w-[80%] transition-all duration-300 "></div>
        </li>
    </ul>
    <!-- <img src="" alt=""> -->
  </header>
  
</template>

<script setup>
const nav = [
    'Home', "About Us", "Services", "Projects", "Contact"
]
const activeLink = useState("activeLink", ()=> "Home");

</script>

<style>

</style>