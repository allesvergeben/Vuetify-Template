<template>
    <v-img
        :height="$vuetify.breakpoint.smAndDown ? 'calc(100vh - 66px - 56px)' : 'calc(100vh - 66px - 64px)'"
        src="https://laurindoerre.de/img/Coding.680796c6.jpg"
        :gradient="this.$vuetify.theme.dark ? 'to top, rgba(44,44,44, .85), rgba(55, 55, 55, .85)' : ''"
    >
        <v-container fill-height>
                <v-sheet
                        color="transparent"
                        max-width="500"
                        class="text-style"
                >
                    <h1
                            class="mb-4"
                            :class="$vuetify.breakpoint.mdAndUp ? 'display-2' : 'display-1'"
                            v-text="$t('home.hero.title')"
                    />
                    <p class="title font-weight-light" v-html="$t('home.hero.description')" />

                </v-sheet>
        </v-container>
    </v-img>
</template>

<script>
    export default {
        name: "Hero",
        data: () => ({
        }),
    }
</script>

<style lang="stylus" scoped>

</style>
