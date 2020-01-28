<template>
    <v-img
        height="calc(100vh - 66px - 64px)"
        src="https://laurindoerre.de/img/Coding.680796c6.jpg"
    >
        <v-container fill-height>
                <v-sheet
                        color="transparent"
                        max-width="500"
                >
                    <h1
                            class="mb-4"
                            :class="$vuetify.breakpoint.mdAndUp ? 'display-2' : 'display-1'"
                    >
                        {{ $t('home.hero.title') }}
                    </h1>

                    <p class="title font-weight-light">
                        {{ $t('home.hero.description') }}
                    </p>
                </v-sheet>
        </v-container>
    </v-img>
</template>

<script>
    export default {
        name: "Hero"
    }
</script>

<style lang="stylus" scoped>
    h1, p
        color var(--v-primary-darken3)
</style>
