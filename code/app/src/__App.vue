<template>
    <HelloWorld>

    </HelloWorld>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';

    HelloWorld
    export default {
        name: 'App',
        components: {
            HelloWorld
        },

        data() {
            return {

            }
        }
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