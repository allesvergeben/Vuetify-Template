<template>
    <v-app>

        <core-app-bar/>

        <v-content>
            <router-view/>
        </v-content>

        <core-footer/>

    </v-app>
</template>

<script>

    export default {
        name: 'App',

        components: {
            CoreFooter: () => import('./components/Core/AppBar'),
            CoreAppBar: () => import('./components/Core/Footer'),
        },

        data: () => ({
            //
        }),
    };
</script>
