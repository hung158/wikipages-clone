<template>
   <main style="color: rgba(47, 47, 47, 1);" class="sm:w-full pt-[72px] mx-auto flex flex-col justify-center items-center  bg-white w-[90%] ">
        <div class=" sm:mx-auto sm:px-12 py-[72px] sm:max-w-[1280px]  ">
            <div>
                <span style="font-family: 'Noto Emoji', Arial;font-weight: 700; color: rgba(47, 47, 47, 1);" class="text-[24.0pt]">🔨</span>
                <!-- <font-awesome-icon class="text-left text-[24.0pt]] " :icon="['fas', 'hammer']" /> -->
            </div>
            <span class="font-bold text-[28px] sm:text-[24.0pt] block " >
                Tasks.co
            </span>
            <span class="text-[18.0pt] block leading-10">
                Work Assignments
            </span>
           <div class="sm:grid sm:grid-cols-3 leading-8">
            <span class="mt-2 text-[14.0pt] block col-span-2 ">
                Make sure things get done around the office and keep track of who is responsible. This is a sample task type page for sites and everything is drag and drop so you can quickly reorganize.
            </span>
           </div>
            
            <div class="grid sm:grid-cols-3 grid-cols-1 gap-x-4 pt-[72px] ">
                <div class="" v-for="item in listData" :key="item.id">
                    <div class="pt-5 pb-6"  >
                        <span  style="font-family: 'Noto Emoji', Arial;font-weight: 700; color: rgba(47, 47, 47, 1);" class="text-[16.0pt] pr-1" :style="{backgroundColor: item.bgColor}">{{ item.img }}</span>
                        <!-- <font-awesome-icon class="text-[16.0pt] pr-1" :style="{backgroundColor: item.bgColor}" :icon="item.img" /> -->
                        <span class="font-bold text-[14.0pt]" :style="{backgroundColor: item.bgColor}">{{ item.name }}</span>
                    </div>
                    
                    <span class="pt-3 text-[14.0pt] font-bold">
                        {{ item.title }}
                    </span>

                    <div class="mt-2 text-[20px]  font-sans">
                        <span style="font-family: 'Noto Emoji', Arial;font-weight: 700; color: rgba(47, 47, 47, 1);">{{ item.icon }}</span>
                        <!-- <font-awesome-icon class="mr-2" :icon="item.icon" /> -->
                        <span>{{ item.subtitle }}</span>
                    </div>

                    <span class="mt-2 text-[20px]  font-sans">
                        {{ item.text }}
                    </span>
                </div>
            </div>
           <div class="grid sm:grid-cols-3 grid-cols-1 mt-6 gap-4 justify-items-center  ">
            <div></div>
            <div class="col-span-1" v-for="item in listData1" :key="item.id">
                    
                    <span class="pt-3 text-[20px]  font-bold">
                        {{ item.title }}
                    </span>

                    <div class="mt-2 text-[20px]  font-sans">
                        <span style="font-family: 'Noto Emoji', Arial;font-weight: 700; color: rgba(47, 47, 47, 1);">{{ item.icon }}</span>
                        <!-- <font-awesome-icon class="mr-2" :icon="item.icon" /> -->
                        <span>{{ item.subtitle }}</span>
                    </div>

                    <span class="mt-2 text-[20px]  font-sans">
                        {{ item.text }}
                    </span>
            </div>
           </div>
        </div>
        
   </main>

   <div style="color: rgba(47, 47, 47, 1);" class="sm:w-full mx-auto ] flex flex-col justify-center items-center  bg-[#f9f9f9] ">
            <div class=" w-[90%] sm:mx-auto sm:px-12 py-[72px] sm:max-w-[1280px]">
                <div class="text-[18.0pt]">
                    <span style="font-family: 'Noto Emoji', Arial;font-weight: 700; color: rgba(47, 47, 47, 1);"class="mr-2 ">🗃️</span>
                    <!-- <font-awesome-icon class="mr-2 " :icon="['fas', 'file']" /> -->
                    <span >Archive of Tasks</span>
                </div>

                <span class="text-[14.0pt] mt-2 block">
                    Collaborate on long-term projects with teams or specific groups. 
                </span>

                <div class="col-span-1" v-for="item in listData2" :key="item.id">
                    <span class="pt-6 text-[14.0pt] block  font-bold">
                        {{ item.title }}
                    </span>

                    <div class="mt-2 text-[14.0pt] font-normal block">
                        <span style="font-family: 'Noto Emoji', Arial;font-weight: 700; color: rgba(47, 47, 47, 1);">{{ item.icon }}</span>
                        <!-- <font-awesome-icon class="mr-2" :icon="item.icon" /> -->
                        <span>{{ item.subtitle }}</span>
                    </div>

                    <span class="mt-2 text-[14.0pt] font-normal block">
                        {{ item.text }}
                    </span>
                </div>
            </div>
    </div>
</template>
<script setup>
import { icon } from '@fortawesome/fontawesome-svg-core';
import { ref } from 'vue';

const listData = ref([
    {
        id:1,
        bgColor: '#f4cccc',
        name:'Not Started',
        title:'Task Title Write Job Descriptions',
        icon:'🙋',
        subtitle:'Bill Trask',
        text:'If you need a description of the tasks go ahead and write something here or link out.',
        img:'🛑',
    },
    {
        id:2,
        bgColor: '#fff2cc',
        name:'In Progress',
        title:'Task Title Write Job Descriptions',
        icon: '🙋',
        subtitle:'Bill Trask',
        text:'If you need a description of the tasks go ahead and write something here or link out.',
        img:'👷',
    },
    {
        id:3,
        bgColor: '#d9ead3',
        name:'Completed',
        title:'Task Title Write Job Descriptions',
        icon:'🙋',
        subtitle:'Bill Trask',
        text:'If you need a description of the tasks go ahead and write something here or link out.',
        img:'🌳',
    },
    {
        id:4,
        name:'',
        title:'Task Title Write Job Descriptions',
        icon:'🙋',
        subtitle:'Bill Trask',
        text:'If you need a description of the tasks go ahead and write something here or link out.'
    },
    {
        id:5,
        name:'',
        title:'Task Title Write Job Descriptions',
        icon:'🙋',
        subtitle:'Bill Trask',
        text:'If you need a description of the tasks go ahead and write something here or link out.'
    },
   
]);
const listData1 = ref([
{
        id:6,
        name:'',
        title:'Task Title Write Job Descriptions',
        icon:'🙋',
        subtitle:'Bill Trask',
        text:'If you need a description of the tasks go ahead and write something here or link out.'
    },
]);

const listData2 = ref([
    {
        id:7,
        name:'',
        title:'Task Title Write Job Descriptions',
        icon:'🙋',
        subtitle:'Bill Trask',
        text:'If you need a description of the tasks go ahead and write something here or link out.'
    },
    {
        id:8,
        name:'',
        title:'Task Title Write Job Descriptions',
        icon:'🙋',
        subtitle:'Bill Trask',
        text:'If you need a description of the tasks go ahead and write something here or link out.'
    },
])

</script>