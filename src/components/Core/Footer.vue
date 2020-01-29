<template>
    <v-footer
            app
            class="elevation-12"
            color="primary"
            height="66"
    >
        <v-layout justify-center>
            <span class="mr-2" > &copy; {{ new Date().getFullYear() }}. All rights reserve </span>
        </v-layout>

    </v-footer>
</template>

<script>
    export default {
        name: "CoreFooter",
        data: () => ({

        }),
    }
</script>

<style scoped>

</style>
