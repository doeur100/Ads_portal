<template>
    <div class="pb-10">
        <div class="grid grid-cols-2 lg:grid-cols-4 gap-[1.5rem] w-[100%]">
            <div v-for="i in 4" class=" bg-[#2A2D3E] h-[14rem] rounded-lg text-white p-[2rem]">
                <div class="flex justify-between" >
                    <span>Budget</span>
                    <span class="material-symbols-outlined">
                        grid_view
                    </span>
                </div>
                <div class="flex flex-col mt-7">
                    <span class="text-5xl flex flex-row justify-center items-center ">900</span>
                    <span class="flex justify-center text-[#F4CE14] text-[0.9rem]">23.12%</span>
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
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-[1.5rem] w-[100%] py-[1.5rem]">
            <div><DAU/></div>
            <div><MAU/></div>
            <div><ChartsRequestAdmin/></div>
            <div><ChartsClickAdmin/></div>
        </div>
        <div>
            <DataListHome/>
        </div>
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