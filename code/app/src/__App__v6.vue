<template>
    <div>
        <TheHeaderVue>
            <template v-slot:title>
                <h1>Sequência</h1>
            </template>
            <template v-slot:description>
                <p>Segue em anexo:</p>
            </template>
        </TheHeaderVue>
    </div>
</template>

<script>
import TheHeaderVue from './components/TheHeader.vue';
export default {
    name: 'App',
    components: { TheHeaderVue },

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