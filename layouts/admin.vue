<template>
    <div>
         <Navbar/>
         <div class="admin-content">
            <Nuxt />
        </div>

    </div>
</template>

<script>
import Navbar from "../components/Navbar.vue";

    export default {
         components: { Navbar }
        
    }
</script>

<style lang="scss" scoped>
div.admin-content {
    margin-left: 250px;
    margin-top: 72px;
    padding: 20px 20px;
    min-height: calc(100vh - 72px);
}

</style>