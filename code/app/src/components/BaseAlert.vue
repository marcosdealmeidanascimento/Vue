<template>
    <div class="['alert', {'alert-success': variant}]">
        C
    </div>
</template>

<script>
    export default {
        props: [
            'variant'
        ]
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
</style>