<template>
    <span>{{message}}</span>
    <br>
    <input v-bind:value="message"/>
</template>

<script setup>
    const message='hello world'
    const color='LightCoral'
</script>

<style>
span {
    color: v-bind('color');
}
</style>
