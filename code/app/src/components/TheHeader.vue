<template>
    <header class="header">
        Header
    </header>
</template>

<script>
export default {
    // Destruir as Libs e Event Listeners
    mounted() {
        window.addEventListener('resize', this.resize)
    },

    beforeUnmount() {
        console.log('beforeUnmount')
    },

    unmounted() {
        console.log('unmounted')
    },

    methods: {
        resize($evt) {
            console.log($evt)
        }
    }
}
</script>

<style>
    .header {
        background-color: #578768;
        color: #fff;
    }
</style>