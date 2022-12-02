<template>
    <div>
        <button @click="onClick" type="submit">Botao</button>
        <p>{{ fullName }}</p><br><br>
        <div v-for="todo in completedTodos"
        :key="todo.id">
            {{ todo.title }} <span> {{ todo.completed }}</span>
        </div>
        <br><br><br><br>
        <div v-for="todo in uncompletedTodos"
        :key="todo.id">
            {{ todo.title }} <span> {{ todo.completed }}</span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'App',

    data() {
        return {
            user: {
                first_name: 'A',
                last_name: 'B'
            },

            todos: [
                {
                    "userId": 1,
                    "id": 1,
                    "title": "delectus aut autem",
                    "completed": false
                },
                {
                    "userId": 1,
                    "id": 2,
                    "title": "quis ut nam facilis et officia qui",
                    "completed": false
                },
                {
                    "userId": 1,
                    "id": 3,
                    "title": "fugiat veniam minus",
                    "completed": false
                },
                {
                    "userId": 1,
                    "id": 4,
                    "title": "et porro tempora",
                    "completed": true
                },
                {
                    "userId": 1,
                    "id": 5,
                    "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
                    "completed": false
                }
                ]
        }
    },

    computed: {
        fullName() {
            return `${this.user.first_name} ${this.user.last_name}`  
        },

        completedTodos() {
            return this.todos.filter(todo => todo.completed)
        },
        
        uncompletedTodos() {
            return this.todos.filter(todo => !todo.completed)
        }
    },

    methods: {
        onClick(){
            console.log(this.fullName)
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
