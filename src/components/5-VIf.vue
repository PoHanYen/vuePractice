<template>
<h1>v-if</h1>
<button @click="isShow1=!isShow1">Toggle</button>  
<div>isShow1:{{isShow1}}</div>
<div v-if="isShow1">Hello!</div>

<h1>v-show</h1>
<button @click="isShow2=!isShow2">Toggle</button>  
<div>isShow1:{{isShow2}}</div>
<div v-if="isShow2">Hello!</div>  

</template>

<script setup>
import {ref} from 'vue'
const isShow1=ref(true)
const isShow2=ref(true)
</script>