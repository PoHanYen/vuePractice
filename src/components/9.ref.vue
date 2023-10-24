<template>
    <div>number {{number}}</div>
    <div>String {{string}}</div>
    <div>array {{array}}</div>
    <div>object {{object}}</div>
<button @click="count++">+1</button>
<div>{{count}}</div>
</template>

<script setup>
import {ref} from 'vue'
const number =ref(1)
const string =ref('this is a String')
const array =ref(['a','b','c'])
const object= ref({name:"bella",id:"2212015"})
const count = ref(0);
</script>
