<template>
    <div>
        <TheHeaderVue v-if="showHeader"/>
        <h2>Teste h2</h2>
        <input v-model="name" type="text">
        <h3>{{ name }}</h3>
        <button @click="showHeader = !showHeader">
            Toggle Header
        </button>
    </div>
</template>

<script>
import TheHeaderVue from './components/TheHeader.vue';
export default {
    name: 'App',
    components: { TheHeaderVue },

    data() {
        return {
            name: 'Teste',
            showHeader: true
        }
    },

    watch: {
    },

    computed: {
    },

    methods: {
    },

    
    beforeUpdate() {
        console.log('beforeUpdate')
    },

    updated() {
        console.log('updated')
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