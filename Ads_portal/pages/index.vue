<template>
        <div class="grid grid-cols-2 lg:grid-cols-4 gap-[1.5rem] w-[100%]">
            <div v-for="i in 4" class=" bg-[#2A2D3E] h-[10rem] rounded-lg text-white">
                <div class="flex justify-between ml-[2rem] mr-[2rem] mt-[1rem]" >
                    <span>Budget</span>
                    <span class="material-symbols-outlined">
                        grid_view
                    </span>
                </div>
                <div class=" ">
                    <span class="text-3xl flex justify-center mt-7">100</span>
                    <span class="flex justify-center text-[15px] mt-4">This is budget from last month</span>
                </div>
            </div>
        </div>
        <div class="flex justify-between mt-[1.5rem]">
            <div class="flex text-white" >
                <input type="date" class="p-2 w-[8rem] rounded-lg mr-5 bg-[#2A2D3E] ">
                <span class="material-symbols-outlined text-white flex items-center">
                    arrow_right_alt
                </span>
                <input type="date" class="p-2 w-[8rem] rounded-lg ml-5 bg-[#2A2D3E]">
            </div>
            <div>
                <button class="bg-[#2A2D3E] text-white mr-5 p-2 w-[8rem]  rounded-lg">Search</button>
                <button class="bg-[#2A2D3E] text-white p-2 w-[8rem] rounded-lg">Export</button>
            </div>
        </div>
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-[1.5rem] w-[100%] py-[1.4rem]">
            <div class=""><DAU/></div>
            <div class="h-[20rem]  bg-[#2A2D3E] rounded-lg"><MAU/></div>
            <div class="h-[20rem]  bg-[#2A2D3E] rounded-lg"><ChartsRequestAdmin/></div>
            <div class="h-[20rem]  bg-[#2A2D3E] rounded-lg mb-10"><ChartsClickAdmin/></div>
        </div>
</template>

<script setup lang="ts" >
    import DAU from "../components/charts/DAU.vue";
    import MAU from "~/components/charts/MAU.vue";
</script>

<style>
  input[type="date"] {
    color-scheme: dark;
  }
</style>