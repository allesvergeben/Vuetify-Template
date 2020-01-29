<template>
    <v-footer
            app
            class="elevation-12"
            color="primary"
            height="66"
    >


                    <div class="caption pr-md-12">
                        &copy;{{ new Date().getFullYear() }}. All rights reserved
                    </div>

          <v-spacer/>
                <v-btn
                        class="mr-10"
                        text
                        aria-label="About"
                        to="/about"
                >
                    About
                </v-btn>

    </v-footer>

</template>

<script>
    export default {
        name: "CoreFooter",
        data: () => ({

        }),
    }
</script>

<style scoped>

</style>
