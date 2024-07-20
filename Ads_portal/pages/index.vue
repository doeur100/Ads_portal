<template>
        <div class="grid grid-cols-2 lg:grid-cols-4 gap-[1.5rem] w-[100%]">
            <div v-for="i in 4" class=" bg-[#2A2D3E] h-[10rem] rounded-lg"></div>
        </div>
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-[1.5rem] w-[100%] py-[1.4rem]">
            <div class=""><DAU/></div>
            <div class="h-[20rem]  bg-[#2A2D3E] rounded-lg"><DAU/></div>
            <div class="h-[20rem]  bg-[#2A2D3E] rounded-lg"></div>
            <div class="h-[20rem]  bg-[#2A2D3E] rounded-lg"></div>
        </div>
</template>

<script setup lang="ts" >
    import DAU from "../components/charts/DAU.vue";
</script>