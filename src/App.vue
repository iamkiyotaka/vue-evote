<template>
  <div class="flex flex-col justify-between min-h-screen">
    <header class="bg-white shadow" v-if="$route.meta.title !=='login'">
      <div class="px-4 py-6 mx-auto max-w-7xl sm:px-6 lg:px-8">
        <div class="container flex justify-between mx-auto">
          <a href="/">
            <img src="@/assets/logo.png" alt="logo evote" srcset="">
          </a>
          <div class="hidden grid-cols-4 text-xl font-medium text-center font-Poppins sm:inline-grid">
            <a href="Calon" class="px-4">Calon</a>
            <a href="Timeline" class="px-4">Timeline</a>
            <a href="Vote" class="px-4">Voting</a>
            <a href="Login" class="px-4"><LogoutIcon class="h-8 mx-auto w-7"/></a>
          </div>
          <NavbarMenu class="inline sm:hidden"></NavbarMenu>
        </div>
      </div>
    </header>
    <main>
      <router-view />
    </main>
    <footer class="bg-main" v-if="$route.meta.title !=='login'">
      <div class="px-4 py-6 mx-auto max-w-7xl sm:px-6 lg:px-8">
        <div class="container flex items-center justify-between">
          <h1 class="inline-block text-lg text-white align-bottom font-Poppins">© 2021 Evote</h1>
          <img src="@/assets/logo.png" alt="logo evote" srcset="">
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
import NavbarMenu from '@/components/NavbarMenu.vue';
import { LogoutIcon } from '@heroicons/vue/outline';
</script>