<template>
  <div class="mt-2">
    <div class="flex justify-between">
      <span class="material-symbols-outlined text-white">west</span>
      <button
        class="bg-[#2A2D3E] flex items-center p-2 rounded-[10px] w-[10rem] justify-center text-white"
      >
        <span class="material-symbols-outlined">add</span>Create User
      </button>
    </div>
    <!-- <AppTable class="mt-10"/> -->
    <div class="bg-[#2A2D3E] main-table pb-10 mt-10">
      <h1 class="text-[#F4CE14] p-5 ml-4">Users</h1>
      <table>
        <tr>
          <th>No.</th>
          <th>Profile</th>
          <th>Username</th>
          <th>Email</th>
          <th>Role</th>
          <th>Status</th>
          <th>Action</th>
        </tr>
        <tr>
          <td>1</td>
          <td>
            <div class="flex justify-center">
              <img
                src="https://marketplace.canva.com/EAFOWUXOOvs/1/0/1600w/canva-green-gradient-minimalist-simple-instagram-profile-picture-tBlf3wVYGhg.jpg"
                alt=""
              />
            </div>
          </td>
          <td>Phannit Phouy</td>
          <td>phannit@gmail.com</td>
          <td class="text-red-500">admin</td>
          <td>
            <span class="bg-green-500 rounded-[20px] pl-10 pr-10 pt-2 pb-2">
              Active
            </span>
          </td>
          <td>
            <div class="flex flex-row justify-evenly">
              <span class="material-symbols-outlined text-red-500"
                >archive</span
              >
              <span class="material-symbols-outlined text-green-500">edit</span>
            </div>
          </td>
        </tr>
        <tr>
          <td>2</td>
          <td>
            <div class="flex justify-center">
              <img
                src="https://marketplace.canva.com/EAFOWUXOOvs/1/0/1600w/canva-green-gradient-minimalist-simple-instagram-profile-picture-tBlf3wVYGhg.jpg"
                alt=""
              />
            </div>
          </td>
          <td>Doeur Diet</td>
          <td>dietdoeur@gmail.com</td>
          <td>customer</td>
          <td>
            <span class="bg-green-500 rounded-[20px] pl-10 pr-10 pt-2 pb-2">
              Active
            </span>
          </td>
          <td>
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
  border-radius: 100px;
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
