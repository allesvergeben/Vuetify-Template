<template>
    <v-app-bar
            app
            color="primary"
    >
        <v-btn @click="toggleDrawer" class="hidden-md-and-up" icon>
            <v-icon>mdi-menu</v-icon>
        </v-btn>
        <div class="d-flex align-center">
            <v-img
                    alt="Vuetify Logo"
                    class="shrink mr-2"
                    contain
                    src="../../assets/example-logo.png"
                    transition="scale-transition"
                    width="40"
                    v-on:click="$router.currentRoute.path === '/' ? '' : $router.push('/')"
            />
        </div>
        <v-spacer/>
        <v-toolbar-items>
            <v-btn
                    href="https://github.com/vuetifyjs/vuetify/releases/latest"
                    target="_blank"
                    text
                    class="hidden-xs-only"
            >
                <span class="mr-2">Vuetify - Latest Release</span>
                <v-icon>mdi-open-in-new</v-icon>
            </v-btn>
            <v-menu offset-y>
                <template v-slot:activator="{ on }">
                    <v-btn
                            icon
                            v-on="on"
                    >
                        <v-icon
                        >
                            mdi-web
                        </v-icon>
                    </v-btn>
                </template>
                <v-list v-model="$i18n.locale">
                    <v-list-item
                            :disabled="$i18n.locale === 'en'"
                            @click="$i18n.locale = 'en'"
                    >
                        <v-list-item-title>English</v-list-item-title>
                    </v-list-item>
                    <v-list-item
                            :disabled="$i18n.locale === 'de'"
                            @click="$i18n.locale = 'de'"
                    >
                        <v-list-item-title>Deutsch</v-list-item-title>
                    </v-list-item>
                </v-list>
            </v-menu>
            <v-btn @click="setTheme" icon>
                <v-icon>mdi-invert-colors</v-icon>
            </v-btn>
        </v-toolbar-items>
    </v-app-bar>
</template>

<script>
    import {mapMutations} from 'vuex'

    export default {
        name: "CoreAppBar",
        methods: {
            ...mapMutations(['toggleDrawer']),
            setTheme() {
                if (this.$vuetify.theme.dark) {
                    return (this.$vuetify.theme.dark = false);
                } else {
                    return (this.$vuetify.theme.dark = true);
                }
            }
        },

    }
</script>

<style scoped>

</style>
