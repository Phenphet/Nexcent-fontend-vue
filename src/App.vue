<script setup>
  import { ref } from 'vue' 
  import { RouterLink, RouterView } from 'vue-router'

  import IconArrowRight from './components/icons/IconArrowRight.vue'

  const menu = ref([
    {name:'Home'},
    {name:'Features'},
    {name:'Community'},
    {name: 'Blog'},
    {name: 'Pricing'}
  ])
</script>

<template >
  <header>
    <div class="container w-full mx-auto flex justify-between items-center px-6">
      <div class="flex flex-row items-center">
        <div class="w-full">
          <img src="./assets/image/Icon.png" alt="icon_nav" width="40" height="40">
        </div>
        <h1 class="text-2xl font-bold">Nexcent</h1>
      </div>
      <div class="flex items-center justify-center mt-2 px-2 md:px-0 md:mt-5 gap-3">
        <nav class="text-xl hidden md:block">
          <ul class=" flex flex-row gap-6 me-5">
            <li v-for="item in menu">
              <a :href="item.name">{{ item.name }}</a>
            </li>
          </ul>
        </nav> 
        <button class="flex flex-row items-center justify-center py-2 px-3  md:py-3 md:px-4 bg-[#4CAF4F] rounded-md text-white gap-2 text-[15px] md:text-md hover:bg-[#156517]">Register Now <IconArrowRight class="hidden md:block mt-1" /></button>
      </div>
    </div>
  </header>
  <RouterView />
</template>

<style scoped>

</style>
