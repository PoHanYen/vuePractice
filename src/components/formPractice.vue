<template>
    <div sytle="width:70%; margin:auto">
    <h1>UserData</h1>
    <el-form :model="form" label-width="120px">
      <el-form-item label="Name">
        <el-input v-model.trim="form.name" />
      </el-form-item>
      <el-form-item label="Age">
        <el-input v-model.number="form.age" />
      </el-form-item>
      <el-form-item label="Gender">
        <el-select v-model="form.gender" placeholder="Gender">
          <el-option label="Male" value="male" />
          <el-option label="Female" value="female" />
        </el-select>
      </el-form-item>
      <el-form-item label="Date">
        <el-col :span="11">
          <el-date-picker
            v-model="form.date"
            type="date"
            placeholder="Pick a date"
            style="width: 100%"
          />
        </el-col>
      </el-form-item>
      <el-form-item label="Country">
        <el-select v-model="form.country" placeholder="country">
          <el-option label="Taiwn" value="Taiwn" />
          <el-option label="Japan" value="Japan" />
          <el-option label="US" value="US"/>
'         <el-option label="Korea" value="Korea" />
        </el-select>
     </el-form-item>
     <el-form-item>
      <el-button v-if="isShow1" type="primary" @click="onSubmit">Submit</el-button>
      <el-button v-if="!isShow1" type="primary" @click="onReset">reset</el-button>
    </el-form-item>

    </el-form>
    </div> 
  </template>
  
  <script lang="ts" setup>
  import { reactive, ref } from 'vue'
  import type { FormInstance, FormRules } from 'element-plus'

    const ruleFormRef = ref<FormInstance>()
  const isShow1 = ref(true);

  // do not use same name with ref
  const form = reactive({
    name: '',
    date: '',
    age: "",
    gender:'',
    country: '',
  })
  
  const onSubmit = () => {
    isShow1.value=false
        alert('submit!')
  }
  const onReset = () => {
    isShow1.value=true
        alert('reset!')
  }
  </script>
  