
import { NuxtPage } from '#build/components';

import { NuxtPage } from '#build/components';
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

        <NuxtLink to="/apps" class="menu-btn">
            <span class="material-symbols-outlined">
            grid_view
            </span>
          <span>Apps</span>
        </NuxtLink>

        <NuxtLink to="/s" class="menu-btn">
            <span class="material-symbols-outlined"> person </span>
          <span>Users</span>
        </NuxtLink>

        <NuxtLink to="/s" class="menu-btn">
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
        <div class="left">
          <h1>ADS portal</h1>
        </div>
          <h1>Image</h1>
      </div>
      <div class="main bg-red-200">
         <NuxtPage></NuxtPage>
        </div>
    </div>
  </div>
</template>

<style scoped>
.app-bar {
  width: 100%;
}
.sidebar {
  @apply fixed h-full w-[14rem] lg:w-[18rem] text-white bg-[#2A2D3E];
}
.sidebar {
    z-index:100 !important;
} 

.sidebar-title {
  @apply flex flex-col items-center gap-2 border-b py-5;
}
.nav-bar {
  @apply   z-30 fixed left-0 md:left-[14rem] lg:left-[18rem] w-full h-[4rem] px-[2rem];
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
</style>
