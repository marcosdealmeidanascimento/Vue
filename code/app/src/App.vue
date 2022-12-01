<template>
    
    <div class="todos">
        
        <div v-for="(obj, index) in array" v-bind:key="obj.id">
            <img v-if="obj.imgURL" :src="obj.imgURL">
            {{ index }} - {{ obj.title }}
        </div>
        
    </div>

</template>

<script>

export default {
name: 'App',
components: {
    
},
data() {
    return {
        
        array: [
            {
                "userId": 1,
                "id": 1,
                "title": "delectus aut autem",
                "completed": false,
                "imgURL": 'https://dummyimage.com/100x50/ff0/fff'
            },
            {
                "userId": 1,
                "id": 2,
                "title": "quis ut nam et officia qui",
                "completed": false
            },
            {
                "userId": 1,
                "id": 3,
                "title": "fugiat veniam dom minus",
                "completed": false
            },
            {
                "userId": 1,
                "id": 4,
                "title": "et porro dum dum tempora",
                "completed": true
            },
            {
                "userId": 1,
                "id": 5,
                "title": "laboriosam mollitia dome illum",
                "completed": false
            }
        ]
    }
}
}
</script>

<style>
*{
    margin: 0px;
    padding: 0px;
}

#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
}

.todos {
    display: block; 
    margin: 25px;
    padding: 25px;
    background-color: #d7a014;
}

.todos div{
    display: flex;
    justify-content: center;
    color: #fff;
    padding: 20px;
}

.todos img {
    margin: 0px;
}

</style>
