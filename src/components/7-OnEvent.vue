<template>
    <button @click="count++">Add 1</button>
    <div>Count is: {{count}}</div>
    <button @click="Greet('bella')">Greet!</button>
</template>

<script setup>
    import {ref} from 'vue'
    const count =ref(0)
    const Greet = (name) =>{
        if (name==='bella'){
            alert(`Hello ${name}!`)
        } else {
            alert('who are you?')
        }
    }
</script>