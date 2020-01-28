<template>
    <div>
        <Hero />
        <Installed />
        <Start />
    </div>
</template>

<script>
    export default {
        components: {
            Hero: () => import('../components/sections/Hero'),
            Installed: () => import('../components/sections/Installed'),
            Start: () => import('../components/sections/Start')
        },
        name: "Home"
    }
</script>

<style scoped>

</style>
