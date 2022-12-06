<template>
    <div>
        <BaseAlertVue v-if="showAlert" :variant="variant" @close="onClose()">
            {{ text }}
        </BaseAlertVue>
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
                showAlert: true,
                variant: 'success',
                text: 'a',
            }
        },

        watch: {
        },

        computed: {
        },

        methods: {
            onClose() {
                this.showAlert = false,
                alert('OnClose')
            }
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