<template>
    <v-container>
        <v-layout
                text-center
                wrap
        >
            <v-flex xs12>
                <v-img
                        :src="require('../assets/logo.svg')"
                        class="my-3"
                        contain
                        height="200"
                ></v-img>
            </v-flex>

            <v-flex mb-4>
                <h1 class="display-2 font-weight-bold mb-3">
                    {{ $t('home.heading') }}
                </h1>
                <p>
                    <span class="subheading font-weight-regular" v-html="$t('home.subheading')"> </span>
                    <a href="https://community.vuetifyjs.com" target="_blank">{{ $t('home.discord') }}</a>
                </p>
                <p>
                    {{ $t('home.message') }}
                    <a href="https://laurindoerre.de" target="_blank">{{ $t('home.homepage') }}</a>
                </p>
            </v-flex>

            <v-flex
                    mb-5
                    xs12
            >
                <h2 class="headline font-weight-bold mb-3">{{ $t('home.whatsNext.headline') }}</h2>

                <v-layout justify-center>
                    <a
                            :href="next.href"
                            :key="i"
                            class="subheading mx-3"
                            target="_blank"
                            v-for="(next, i) in whatsNext"
                    >
                        {{ next.text }}
                    </a>
                </v-layout>
            </v-flex>

            <v-flex
                    mb-5
                    xs12
            >
                <h2 class="headline font-weight-bold mb-3">{{ $t('home.importantLinks.headline') }}</h2>

                <v-layout justify-center>
                    <a
                            :href="link.href"
                            :key="i"
                            class="subheading mx-3"
                            target="_blank"
                            v-for="(link, i) in importantLinks"
                    >
                        {{ link.text }}
                    </a>
                </v-layout>
            </v-flex>

            <v-flex
                    mb-5
                    xs12
            >
                <h2 class="headline font-weight-bold mb-3">{{ $t('home.ecosystem.headline') }}</h2>

                <v-layout justify-center>
                    <a
                            :href="eco.href"
                            :key="i"
                            class="subheading mx-3"
                            target="_blank"
                            v-for="(eco, i) in ecosystem"
                    >
                        {{ eco.text }}
                    </a>
                </v-layout>
            </v-flex>
        </v-layout>
    </v-container>
</template>

<script>
    export default {
        name: 'HelloWorld',

        data: () => ({}),
        computed: {
            ecosystem() {
                return [
                    {
                        text: this.$t('home.ecosystem.text.0'),
                        href: 'https://github.com/vuetifyjs/vuetify-loader',
                    },
                    {
                        text: this.$t('home.ecosystem.text.1'),
                        href: 'https://github.com/vuetifyjs/vuetify',
                    },
                    {
                        text: this.$t('home.ecosystem.text.2'),
                        href: 'https://github.com/vuetifyjs/awesome-vuetify',
                    },
                ]
            },
            importantLinks() {
                return [
                    {
                        text: this.$t('home.importantLinks.text.0'),
                        href: 'https://vuetifyjs.com',
                    },
                    {
                        text: this.$t('home.importantLinks.text.1'),
                        href: 'https://community.vuetifyjs.com',
                    },
                    {
                        text: this.$t('home.importantLinks.text.2'),
                        href: 'https://madewithvuejs.com/vuetify',
                    },
                    {
                        text: this.$t('home.importantLinks.text.3'),
                        href: 'https://twitter.com/vuetifyjs',
                    },
                    {
                        text: this.$t('home.importantLinks.text.4'),
                        href: 'https://medium.com/vuetify',
                    },
                ]
            },
            whatsNext() {
                return [
                    {
                        text: this.$t('home.whatsNext.text.0'),
                        href: 'https://vuetifyjs.com/components/api-explorer',
                    },
                    {
                        text: this.$t('home.whatsNext.text.1'),
                        href: 'https://vuetifyjs.com/layout/pre-defined',
                    },
                    {
                        text: this.$t('home.whatsNext.text.2'),
                        href: 'https://vuetifyjs.com/getting-started/frequently-asked-questions',
                    },
                ]
            }
        }
    };
</script>
