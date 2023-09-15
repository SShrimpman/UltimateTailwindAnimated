<template>
  <SideBar/>
  <div class="bg-gray-400 dark:bg-gray-600 overflow-hidden">
    <router-view #="{ Component }">
      <transition name="slide" mode="out-in">
        <component :is="Component" :key="$route.path"/>
      </transition>
    </router-view>
  </div>
</template>

<script setup>
import SideBar from './components/SideBar.vue'
</script>

<style>
.slide-enter-active,
.slide-leave-active {
  transition: opacity 0.5s, transform 0.5s;
}

.slide-enter-from {
  opacity: 0;
  transform: translateY(50%)
}

.slide-leave-to {
  opacity: 0;
  transform: translateY(-50%)
}
</style>