<template>
    <div class="box"
    @mouseover="isShow=true"
    @mouseleave="isShow=flase"/>
    <div v-if="isShow">Hello</div>
    <div v-if="isShow">Hello</div>
</template>

<script setup>
    import {ref} from 'vue'
    const isShw = ref(false)
</script>

<style>
</style>