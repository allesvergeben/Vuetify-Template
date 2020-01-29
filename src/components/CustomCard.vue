<template>
    <v-card
        class="custom-card"
    >
        <v-card-subtitle class="pb-0" v-text="step"/>
        <v-card-title v-text="title"/>
        <v-card-subtitle v-text="subtitle"/>
        <v-card-text v-html="text"/>
        <v-divider class="mx-auto" v-if="buttons.length !== 0"/>
        <v-card-actions>
            <v-spacer/>
            <v-btn
                    :href="button.link"
                    target="_blank"
                    :key="i"
                    text
                    v-for="(button, i) in buttons"
                    v-text="button.text"
            />
        </v-card-actions>
    </v-card>
</template>

<script>
    export default {
        name: "CustomCard",
        props: {
            step: {
                type: String,
                default: ''
            },
            title: {
                type: String,
                default: ''
            },
            subtitle: {
                type: String,
                default: ''
            },
            text: {
                type: String,
                default: ''
            },
            buttons: {
                type: Array,
                default: () => ({
                    text: {
                        type: String,
                        default: ''
                    },
                    link: {
                        type: String,
                        default: ''
                    },
                }),
            }
        }
    }
</script>

<style lang="stylus" scoped>
    .custom-card
        .v-divider
            font 1px
</style>
