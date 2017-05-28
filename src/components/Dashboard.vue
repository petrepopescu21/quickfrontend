<template>
    <div class="main">
        <news></news>
        <files></files>
    </div>
</template>

<script>
import News from './News.vue'
import Files from './Files.vue'
export default {
    name: "Dashboard",
    components: {News,Files},
    
}
</script>