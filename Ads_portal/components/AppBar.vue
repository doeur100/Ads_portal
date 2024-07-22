<template>
  <div class="app-bar flex flex-row relative">
    <div class="sidebar">
      <div class="sidebar-title">
        <NuxtLink to="/">
          <div class="sidebar-logo">
            <h1>ADS</h1>
          </div>
        </NuxtLink>
      </div>
      <div class="flex flex-col gap-2 p-3">
        <NuxtLink to="/" class="menu-btn">
          <span class="material-symbols-outlined"> home </span>
          <span>Home</span>
        </NuxtLink>

        <div class="dropdown">
          <NuxtLink to="/apps">
            <div
              class="dropdown-btn cursor-pointer flex flex-row justify-between"
              @click="showApp"
            >
              <div class="flex flex-row items-center gap-2">
                <span class="material-symbols-outlined"> grid_view </span>
                <span class="sidebar-hidden">Apps</span>
              </div>
              <span
                class="material-symbols-outlined"
                :class="{ 'rotate-180': isApp }"
              >
                arrow_drop_down
              </span>
            </div>
            <NuxtLink
              to="/units"
              v-if="isApp"
              class="menu-btn dropdown-item"
              :class="$route.path == '/units' ? 'router-link-active' : ''"
            >
              <span class="material-symbols-outlined"> ad_units </span>
              <span>Ad unit</span>
            </NuxtLink>
          </NuxtLink>
        </div>

        <NuxtLink to="/users" class="menu-btn">
          <span class="material-symbols-outlined"> person </span>
          <span>Users</span>
        </NuxtLink>

        <NuxtLink to="/campaigns" class="menu-btn">
          <span class="material-symbols-outlined"> campaign </span>
          <span>Campaigns</span>
        </NuxtLink>
        <NuxtLink to="/s" class="menu-btn">
          <span class="material-symbols-outlined"> edit_note </span>
          <span>Activity log</span>
        </NuxtLink>
      </div>
    </div>
    <div>
      <div class="nav-bar">
        <div class="left text-white">
          <h1>ADS portal</h1>
        </div>
        <Profile />
      </div>
      <div class="main bg-red-200">
        <NuxtPage></NuxtPage>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import Profile from "./dialogs/Profile.vue";
const isApp = ref(false);
const showApp = () => {
  isApp.value = !isApp.value;
};
</script>
<style scoped>
.app-bar {
  width: 100%;
}
.sidebar {
  @apply fixed h-full w-[14rem] lg:w-[18rem] text-white bg-[#2A2D3E];
}
.sidebar {
  z-index: 100 !important;
}

.sidebar-title {
  @apply flex flex-col items-center gap-2  py-5;
}
.nav-bar {
  @apply md:w-[calc(100%-14rem)] lg:w-[calc(100%-18rem)] z-30 fixed left-0 md:left-[14rem] lg:left-[18rem] w-full h-[4rem] px-[2rem];
  @apply flex justify-between items-center text-black;
}
.nav-bar {
  z-index: 90;
}
.nav-bar .left {
  @apply flex justify-center items-center gap-5;

  span {
    @apply select-none block md:hidden p-2 border rounded-md bg-slate-100 cursor-pointer hover:bg-slate-200;
  }
}

/* //============================// */

.menu-btn,
.main-tool {
  @apply flex flex-row items-center gap-3 rounded-md py-3 px-2 sm:px-5;

  span {
    @apply select-none truncate;
  }
}

.menu-btn.router-link-active {
  @apply bg-[#212332] text-white mx-0;
}

.menu-btn .material-symbols-outlined {
  @apply select-none;
}

.dropdown {
  @apply relative;
}

.dropdown .dropdown-btn {
  @apply flex justify-between items-center gap-3 rounded-md py-3 px-2 sm:px-5 cursor-pointer;

  span {
    @apply select-none;
  }
}

.dropdown .dropdown-item {
  @apply ml-8 px-3;

  span {
    @apply select-none;
  }
}
</style>
