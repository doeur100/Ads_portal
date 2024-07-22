<template>
    <div class="mt-2">
      <div class="flex justify-between">
        <span class="material-symbols-outlined text-white">west</span>
        <button
          class="bg-[#2A2D3E] flex items-center p-2 rounded-[10px] w-[11rem] justify-center text-white"
        >
          <span class="material-symbols-outlined">add</span>Create Unit
        </button>
      </div>
      <!-- <AppTable class="mt-10"/> -->
      <div class="bg-[#2A2D3E] main-table pb-10 mt-10">
        <h1 class="text-[#F4CE14] p-5 ml-4">Users</h1>
        <table>
          <tr>
            <th>No.</th>
            <th>Name</th>
            <th>Format</th>
            <th>Status</th>
            <th>Action</th>
          </tr>
          <tr>
            <td>1</td>
            <td>Smart</td>
            <td>Banner</td>
            <td class="w-[20rem]">
                <div class="flex justify-center">

                    <div class="bg-green-500 rounded-[20px] w-[8rem] p-1.5">
                        <span >Active</span>
                    </div>
                </div>
            </td>
            <td  class="w-[15rem]">
              <div class="flex flex-row justify-evenly">
                <span class="material-symbols-outlined text-red-500"
                  >archive</span
                >
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
  <style scoped>
  .main-table {
    border-radius: 10px;
  }
  table {
    width: 100%;
  }
  img {
    width: 3rem;
  }
  th {
    border-bottom: 1px solid #4c4c5a;
    border-top: 1px solid #4c4c5a;
  }
  th {
    height: 80px;
    color: #f4ce14;
  }
  td {
    border-bottom: 1px solid #4c4c5a;
    text-align: center;
    color: white;
    height: 70px;
  }
  </style>
  