<template>
    <div class="w-full pt-[72px] h-auto bg-white pb-12 grid grid-cols-1" >
      <div class="h-12"></div>
      <div class="sm:max-w-3xl mx-auto container flex flex-col justify-center items-center  ">
        <div class="sm:px-2 sm:pb-3 sm:w-full w-[90%] " >
            <span class="font-sans text-[24.0pt]">📚</span>
            <span class="font-bold text-[24.0pt] block ">Sites.wiki</span>
          <div class="mt-2">
            <span class="font-normal text-[18.0pt]">About</span>
          </div>
          <div class="mt-2">
            <span class="text-lg">
              Minimalist wiki template powered by Google Sites for your company <br> 
              intranet included in Google Workspace.
            </span>
          </div>
        </div>
  
        <div class="sm:grid sm:grid-cols-2 flex flex-col justify-center items-center  px-2 mt-10 py-3 w-full">
          <div class=" w-[272px]"  v-for="category in dataCategories" :key="category.id">
            <div class="border-bottom py-2 sm:w-[75%]">
              <span style="color: rgba(47, 47, 47, 1);" class="leading-8 font-bold text-[14.0pt]">
              {{ category.title }}
            </span>
            </div>
            <div class="py-[14px] px-2">
              <div class="my-3" v-for="item in category.items" :key="item.name">
              <router-link class="text-[14.0pt]" :to="item.url">
                <span class="mr-2">{{ item.icon }}</span>
                <span style="color: rgba(28, 28, 28, 1);">{{ item.name }}</span>
              </router-link>
            </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
    const dataCategories = ref([
      {
        id: 1,
        title: 'Top Wiki Pages',
        items: [
          {
          name:'Announcements', icon: '⭐️', url:'',
          },
          {
          name:'Company Directory', icon: '💎', url:'',
          },
          {
          name:'Instant Messaging', icon: '🌿', url:'',
          },
          {
          name:'Customer Service', icon: '🍊', url:'',
          },
      ]
      },
      {
        id: 2,
        title: 'New Employees',
        items: [
          {
          name:'Onboarding', icon: '⭐️', url:'',
          },
          {
          name:'Glossary', icon: '💎', url:'',
          },
          {
          name:'FAQ', icon: '🌿', url:'',
          },
          {
          name:'Training', icon: '🍊', url:'',
          },
      ]
      },
      {
        id: 3,
        title: 'Extras',
        items: [
          {
          name:'Scheduling', icon: '💖', url:'',
          },
          {
          name:'Support', icon: '🌈', url:'',
          },
          {
          name:'Pay Stubs', icon: '🎪', url:'',
          },
      ]
      },
      {
        id: 4,
        title: 'News & Updates',
        items: [
          {
          name:'Employee Feedback', icon: '🥳', url:'',
          },
          {
          name:'Calendars', icon: '🌐', url:'',
          },
          {
          name:'Health & Safety', icon: '🌸', url:'',
          },
      ]
      },
      {
        id: 5,
        title: 'Documents',
        items: [
          {
          name:'HR Forms', icon: '🖤', url:'',
          },
          {
          name:'Social ', icon: '🔮', url:'',
          },
          {
          name:'Network', icon: '🌞', url:'',
          },
          {
          name:'Event', icon: '🐠', url:'',
          },
      ]
      },
      {
        id: 6,
        title: 'Social Platforms',
        items: [
          {
          name:'Professional Dev', icon: '🖤', url:'',
          },
          {
          name:'From the CEO', icon: '🔮', url:'',
          },
          {
          name:'Learning System', icon: '🌞', url:'',
          },
          {
          name:'', icon: '', url:'',
          },
      ]
      },
    ])
  </script>
  
  <style scoped>
/* .border-bottom{
  border-bottom: 1px solid black;
} */
</style>