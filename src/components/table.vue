<template>
    <div style="width:70%;margin: auto;">
    <h1>UserData</h1>
    <el-table-item label="UserName:"><el-input v-model="search" si></el-input></el-table-item>
    <el-table :data="tableFilter" height="250" style="width: 100%" :row-class-name="tableRowClassName">
    <el-table-column v-for="(obj,title) in tableData[0]" :key="title" :prop="title" :label="title" width="400"/>
    </el-table>
</div>
  </template>
  
  <script lang="ts" setup>
import { makeList } from 'element-plus';
import {computed,ref} from 'vue'
  const search =ref('')
  const tableFilter = computed(()=>
        tableData.filter((data)=>!search.value||data.name.toLowerCase().includes(search.value))
  )
  const tableData = [
    {
      name: 'Apple',
      date: '1993-05-03',
      age: 19,
      gender: 'male',
      country:'US'
    },
    {
      name: 'Banana',
      date: '1993-05-03',
      age: 29,
      gender: 'female',
      country:'Taiwan'
    },    
    {
      name: 'Citrus',
      date: '1993-05-03',
      age: 39,
      gender: 'female',
      country:'Japan'
    },    
    {
      name: 'David',
      date: '1993-05-03',
      age: 92,
      gender: 'male',
      country:'Korea'
    },
  ]
  interface User {
  date: string
  name: string
  address: string
}
  const tableRowClassName = ({
  row,
  rowIndex,
}: {
  row: User
  rowIndex: number
}) => {
  if (rowIndex%3 === 1) {
    return 'warning-row'
  } else if (rowIndex%3 === 2) {
    return 'success-row'
  }else if (rowIndex%3 === 3) {
    return 'success-row'
  }
}
  
</script>
<style>
.el-table .warning-row {
  --el-table-tr-bg-color: var(--el-color-warning-light-9);
}
.el-table .success-row {
  --el-table-tr-bg-color: var(--el-color-success-light-9);
}
</style>