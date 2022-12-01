<template>
    
    <!-- <div class="todos">
        <h1 :class="{ 'title': true, 'title-home': isHome }">Curso</h1>
        
        <p :class="[pClass, {'subTitle-home': isHome}]">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit facere, laboriosam eligendi deleniti dicta aperiam eius quas nostrum accusamus ipsum est corporis, quaerat hic quia. Voluptas ab maiores iusto omnis.
        </p>
        
        <div v-for="(obj, index) in array" v-bind:key="obj.id">
            <img v-if="obj.imgURL" :src="obj.imgURL">
            {{ index }} - {{ obj.title }}
        </div>
        
    </div> -->


    <div>
        <div>
            <p>A B C</p>
            <p>D E F</p><br>
        </div>

        <div>
            <input v-model="name" type="text">
        </div>
        <p>{{ name }}</p>
        
        
        <div>
            <select v-model="lista">
                <option value=""></option>
                <option value="a">a</option>
                <option value="b">b</option>
                <option value="c">c</option>
            </select>
                
            <br><br>

            <input v-model="newsletter" type="radio" value="yes"> Yes
            <br><br>
            <input v-model="newsletter" type="radio" value="no"> No

            <br><br>

            <input v-model="termo" type="checkbox" value="Sim"> Sim <br>
            {{ termo }}

            <br>
            <input v-model="termos" type="checkbox" value="Yes"> Y
            <input v-model="termos" type="checkbox" value="No"> N
            <input v-model="termos" type="checkbox" value="Maybe"> M
            <input v-model="termos" type="checkbox" value="Would"> W
            <br>
            {{ termos }}
        </div>
    </div>
    {{ newsletter }}
</template>

<script>

export default {
name: 'App',
components: {
    
},
data() {
    return {
        // Declaração das binds

        name: ' ',
        lista: 'a',
        newsletter: '',
        termo: '',
        termos: [],

        // varTitle: 'title', // O 'title' é o nome da class, que foi colocada como varTitle no h1
        // isHome: true, // Esse valor é o que determina o estado do v-bind
        // pClass: 'text',
        
        
        // array: [
        //     {
        //         "userId": 1,
        //         "id": 1,
        //         "title": "delectus aut autem",
        //         "completed": false,
        //         "imgURL": 'https://dummyimage.com/100x50/ff0/fff'
        //     },
        //     {
        //         "userId": 1,
        //         "id": 2,
        //         "title": "quis ut nam et officia qui",
        //         "completed": false
        //     },
        //     {
        //         "userId": 1,
        //         "id": 3,
        //         "title": "fugiat veniam dom minus",
        //         "completed": false
        //     },
        //     {
        //         "userId": 1,
        //         "id": 4,
        //         "title": "et porro dum dum tempora",
        //         "completed": true
        //     },
        //     {
        //         "userId": 1,
        //         "id": 5,
        //         "title": "laboriosam mollitia dome illum",
        //         "completed": false
        //     }
        // ]
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

/* .title {
    font-size: 25px;
}

.title-home {
    font-size: 40px;
}

.subTitle-home {
    font-size: 25px;
}

.text {
    color: #000fff;
    font-style: italic;
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
} */

</style>
