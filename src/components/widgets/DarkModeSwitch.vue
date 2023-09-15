<template>
    <div class="sidebar-icon select-none" @click="toggleDark()">
        <transition name="fade" mode="out-in"
         enter-active-class="transition-opacity duration-200"
         leave-active-class="transition-opacity duration-200"
         enter-from-class="opacity-0"
         leave-to-class="opacity-0">
            <font-awesome-icon :key="icon" :icon="icon" class="fa-2xl"/>
        </transition>
    </div>
</template>

<script setup>
    import { useDark, useToggle } from "@vueuse/core"
    import { computed } from 'vue'

    const isDark = useDark({ disableTransition: false });
    const toggleDark = useToggle(isDark);
    const icon = computed(() => isDark.value ? "fa-solid fa-sun" : "fa-solid fa-moon")
</script>