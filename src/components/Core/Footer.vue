<template>
    <v-footer
            app
            class="elevation-12"
            color="primary"
            height="66"
    >
        <v-layout justify-center>
            <span class="mr-2" style="color: white"> &copy; {{ new Date().getFullYear() }}. All rights reserve </span>
        </v-layout>

    </v-footer>
</template>

<script>
    export default {
        name: "CoreFooter"
    }
</script>

<style scoped>
    span {
        color: white;
    }
</style>
