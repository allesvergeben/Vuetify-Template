<template>
    <v-navigation-drawer v-model="drawer" app temporary>
        <v-list>
        </v-list>
    </v-navigation-drawer>
</template>

<script>
    export default {
        name: "CoreDrawer",
        computed: {
            drawer: {
                get () {
                    return this.$store.state.drawer
                },
                set (value) {
                    this.$store.commit('setDrawer', value)
                }
            }
        }
    }
</script>

<style scoped>

</style>
