<template>
    <v-container>
        <section-header :header="$t('home.start.header')" :sub-header="$t('home.start.subheader')" />
        <v-row>
            <v-col
                    v-for="(step, i) in steps"
                    :key="i"
                    cols="12"
                    lg="4"
            >
                <custom-card
                        :step="step.step"
                        :title="step.title"
                        :subtitle="step.subtitle"
                        :text="step.text"
                        :buttons="step.buttons"
                />
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
    export default {
        name: "Packages",
        computed: {
            steps () {
                return JSON.parse(JSON.stringify(this.$t('home.start.steps')));
            }
        },
    }
</script>

<style scoped>

</style>
