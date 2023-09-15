<template>
    <div class="sidebar-icon group">
        <font-awesome-icon :icon="icon"/>
        <span class="sidebar-tooltip group-hover:scale-100">
            {{ text }}
        </span>
    </div>
</template>

<script>
    export default {
        props: {
            icon: {
                type: String,
                required: true,
            },
            text: {
                type: String,
                required: true,
            }
        }
    }
</script>