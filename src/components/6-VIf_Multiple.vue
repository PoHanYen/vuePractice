<template>
    <button @click="count++">+1</button>
    <div v-if="count===1"> count = 1 </div>
    <div v-else-if="count===2"> count = 1 </div>
    <div v-else> count = N </div>

</template>
<script setup>
    import {ref} from 'vue'
    const count=ref(1)
</script>