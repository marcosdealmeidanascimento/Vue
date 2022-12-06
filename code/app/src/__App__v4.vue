<template>
    <div>
        <input v-model="name" type="text">
        <br>
        {{ name }}
    </div>
    <div>
        <select v-model="pageCount">
            <option value="5">5</option>
            <option value="10">10</option>
            <option value="15">15</option>
        </select>
        {{ pageCount }}
    </div>
    <div>
        <input v-model="user.first_name" type="text">
        <input v-model="user.last_name" type="text">
        {{ user.first_name}} {{ user.last_name}}
    </div>
</template>

<script>

    export default {
        name: 'App',

        data() {
            return {
                name: "",
                pageCount: 5,
                user: {
                    first_name: "",
                    last_name: ""
                }
            }
        },

        watch: {
            name(newValue) {
                // console.log(newValue, oldValue)
                if (newValue.length == 5) {
                    this.saveUsername()
                }
            },

            pageCount() {
                this.changePage()
            },
            user: {
                handler() {
                    console.log('User Alterado')
                },
                deep: true
            }
        },

        computed: {
        },

        methods: {
            saveUsername() {
                console.log(this.name);
            },

            changePage() {
                console.log('sa')
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
