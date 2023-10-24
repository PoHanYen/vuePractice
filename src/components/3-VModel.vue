<template>
    <span>{{message}}</span>
    <input v-model.trim="message"/>
</template>

<script setup>
    import {ref} from 'vue'
    const message = ref('hellow World')
</Script>