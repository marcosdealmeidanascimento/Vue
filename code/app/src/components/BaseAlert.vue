<template>
    <div :class="(baseClass)">
        {{ text }}

        <button @click="onClick()">Ø</button>
    </div>
</template>

<script>
    export default {
        props: {
            variant: {
                type: String,
                default: ''
            },

            text: {
                type: String,
                default: 'Text'
            }
        },

        computed: {
            baseClass() {
                return ['alert', this.variant ? `alert-${this.variant}`: '']
            },

        },

        methods: {
            onClick() {
                this.$emit('close')
            }
        }
    }
</script>

<style scoped>

* {
    text-align: center;
}

.alert {
    background-color: #ddd;
    color: #444;
    border-radius: 10px;
}

.alert-success {
    background-color: #53db67;
    color: #fff;
    border-radius: 90px;
    transition: 5s;
}

.alert-danger {
    background-color: #922;
    color: #fff;
    border-radius: 5px;
    transition: 2s;
}
</style>