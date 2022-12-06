<template>
    <header class="header">
        <slot v-if="$slots.title" name="title"></slot>
        <slot name="description"></slot>
    </header>
</template>

<script>
export default {
}
</script>

<style>
    .header {
        background-color: #000;
        color: #fff;
    }
</style>