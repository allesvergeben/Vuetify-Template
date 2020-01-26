<template>
    <v-app-bar
            app
            color="primary"
            dark
    >
        <div class="d-flex align-center">
            <v-img
                    alt="Vuetify Logo"
                    class="shrink mr-2"
                    contain
                    src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
                    transition="scale-transition"
                    width="40"
            />

            <v-img
                    alt="Vuetify Name"
                    class="shrink mt-1 hidden-sm-and-down"
                    contain
                    min-width="100"
                    src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
                    width="100"
            />
        </div>

        <v-spacer></v-spacer>
        <v-toolbar-items>
            <v-btn
                    href="https://github.com/vuetifyjs/vuetify/releases/latest"
                    target="_blank"
                    text
            >
                <span class="mr-2">Latest Release</span>
                <v-icon>mdi-open-in-new</v-icon>
            </v-btn>
            <v-menu offset-y>
                <template v-slot:activator="{ on }">
                    <v-btn
                            icon
                            v-on="on"
                    >
                        <v-icon
                                color="white"
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
        </v-toolbar-items>
    </v-app-bar>
</template>

<script>
    export default {
        name: "CoreAppBar"
    }
</script>

<style scoped>

</style>
