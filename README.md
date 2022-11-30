# Vue.js

## Componente Único

```js
<template>
    <div>
        <h1 class='title'>
            {{ title }}
        </h1>
    </div>
</template>

<script>
    export default{
        name: 'MyComponent',

        data() {
            return {
                title: 'Ainda Não Seguirei',
            };
        },

        methods: {},
    };
</script>

<style>
.title {
    font-size: 20px;
}
</style>
```

### Exemplo


**_index.html_**

```js
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="https://unpkg.com/vue@3"></script>
</head>
<body>
    <div id="app">{{ message }}</div>

    <script src="app.js"></script>
</body>
</html>
```


**_app.js_**

```js
const { createApp } = Vue

createApp({
    data() {
        return {
            message: 'Hatred!'
        }
    }
}).mount('#app')
```

### Instalando o npm

[Node](https://nodejs.org/dist/v14.9.0/)

### Instalando o Vue CLI

```
sudo npm install -g @vue/cli
```