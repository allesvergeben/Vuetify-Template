<template>
    <HelloWorld/>
</template>

<script>
    export default {
        components: {
            HelloWorld: () => import('../components/HelloWorld')
        },
        name: "Home"
    }
</script>

<style scoped>

</style>
