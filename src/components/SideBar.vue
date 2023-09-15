<template>
    <div class="fixed top-0 left-0 h-screen w-[75px] flex flex-col bg-gray-500 dark:bg-gray-900 text-white shadow-lg">
        <div v-for="page in pages" :key="page.id">
            <router-link :to="page.link">
                <SideBarIcon :icon="page.icon" :text="page.text" class="fa-2xl"/>
            </router-link>
        </div>
        <DarkModeSwitch/>
    </div>
</template>

<script>
import SideBarIcon from './SideBarIcon.vue';
import DarkModeSwitch from './widgets/DarkModeSwitch.vue';

    export default {
        components: {
            SideBarIcon,
            DarkModeSwitch
        },
        data() {
            return {
                info : {
                    link : "/"
                },
                pages: [
                    {
                        link: "/",
                        icon: "fa-solid fa-fire-flame-curved",
                        text: "To Hello World!"
                    },
                    {
                        link: "/secondpage",
                        icon: "fa-solid fa-plus",
                        text: "To Second Page!"
                    },
                    {
                        link: "/",
                        icon: "fa-solid fa-bolt-lightning",
                        text: "To Hello World!"
                    },
                    {
                        link: "/secondpage",
                        icon: "fa-solid fa-poop",
                        text: "To Second Page!"
                    }
                ]
            }
        },
    }
</script>