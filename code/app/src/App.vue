<template>
    <div>
        <BaseAlertVue variante="success"/>
    </div>
</template>

<script>
    import BaseAlertVue from './components/BaseAlert.vue';
        export default {
            name: 'App',
            components: {
                BaseAlertVue

            },

            data() {
                return {
                }
            },

            watch: {
            },

            computed: {
            },

            methods: {
            },
        }
</script>

<style>
*{
    margin: 0px;
    padding: 20px;
}

#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
}

</style>