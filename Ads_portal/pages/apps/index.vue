<template>
    <div class="mt-2">
        <div class="flex justify-between">
            <span class="material-symbols-outlined text-white">west</span>
            <button class="bg-[#2A2D3E] flex items-center p-2 rounded-[10px] w-[10rem] justify-center text-white"><span class="material-symbols-outlined  ">add</span>Create App</button>
        </div>
        <!-- <AppTable class="mt-10"/> -->
        <div class="bg-[#2A2D3E] main-table pb-10 mt-10">
        <h1 class="text-[#F4CE14] p-5 ml-4">Apps</h1>
        <table>
          <tr>
             <th>Icon</th>
             <th>Name</th>
             <th>Ad unit</th>
             <th>Request</th>
             <th>Impression</th>
             <th>Click</th>
             <th>Status</th>
             <th>Action</th>
          </tr>
          <tr>
             <td><span class="material-symbols-outlined">directions_car</span></td>
             <td>Racing Car</td>
             <td>2 actives</td>
             <td>120</td>
             <td>100</td>
             <td>100</td>
             <td>
                <span class="bg-[#5F6368] rounded-[20px] pl-10 pr-10 pt-2 pb-2">
                Archieved
                </span>
             </td>
             <td>
                <div class="flex flex-row justify-evenly">
                    <span class="material-symbols-outlined text-red-500">archive</span>
                    <span class="material-symbols-outlined text-green-500">edit</span>
                </div>
             </td>
          </tr>
          <tr>
             <td><span class="material-symbols-outlined">directions_car</span></td>
             <td>Racing Car</td>
             <td>2 actives</td>
             <td>120</td>
             <td>100</td>
             <td>100</td>
             <td>
                <span class="bg-[#5F6368] rounded-[20px] pl-10 pr-10 pt-2 pb-2">
                Archieved
                </span>
             </td>
             <td>
                <div class="flex flex-row justify-evenly">
                    <span class="material-symbols-outlined text-red-500">archive</span>
                    <span class="material-symbols-outlined text-green-500">edit</span>
                </div>
             </td>
          </tr>
          <tr>
             <td><span class="material-symbols-outlined">directions_car</span></td>
             <td>Racing Car</td>
             <td>2 actives</td>
             <td>120</td>
             <td>100</td>
             <td>100</td>
             <td>
                <span class="bg-[#5F6368] rounded-[20px] pl-10 pr-10 pt-2 pb-2">
                Archieved
                </span>
             </td>
             <td>
                <div class="flex flex-row justify-evenly">
                    <span class="material-symbols-outlined text-red-500">archive</span>
                    <span class="material-symbols-outlined text-green-500">edit</span>
                </div>
             </td>
          </tr>
          
      </table>
    </div>
    </div>
</template>
<script setup lang="ts">
    // import AppTable from '~/components/tables/AppTable.vue';
</script>
<style>

.main-table{
     border-radius:10px;
  }
 table {
   width:100%;
 }
 th {
     border-bottom: 1px solid #4C4C5A;
     border-top: 1px solid #4C4C5A;
 }
 th {
     height: 80px;
     color:#F4CE14;
 }
 td {
     border-bottom: 1px solid #4C4C5A;
     text-align:center;
     color:white;
     height:70px;
 }
</style>