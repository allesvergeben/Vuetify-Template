<template>
    <v-container>
        <section-header :header="$t('home.install.header')" :sub-header="$t('home.install.subheader')" />
                <v-row>
                <v-col
                        v-for="(plugin, i) in plugins"
                        :key="i"
                        cols="12"
                        lg="3"
                        md="6"
                >
                        <custom-card
                                :title="plugin.title"
                                :subtitle="plugin.subtitle"
                                :text="plugin.text"
                                :buttons="plugin.buttons"
                        />
                </v-col>
        </v-row>
    </v-container>
</template>

<script>
    export default {
        name: "Install",
        data: () => ({

        }),
        computed: {
            plugins () {
                return JSON.parse(JSON.stringify(this.$t('home.install.plugins')));
            }
        },
    }
</script>

<style scoped>

</style>
