<template>
    <div>Array</div>
    <div v-for="(item, index) in productArr" :key="index">
    no {{index}} is {{item}}
    </div>
    <div> object </div>
    <div v-for="item in productObj"  :key="item.name">
        {{item.name}} is {{item.price}} $
    </div>
</template>

<script setup>
const productArr =['a','b','c']
const productObj=[
{name:'chocolate', price:'10'},
{name:'ice cream', price:'20'},
{name:' strawberry', price:'30'}
]
</script>
