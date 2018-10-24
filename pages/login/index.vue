<template>
    <el-row :gutter="20">
      <h1>Login Page</h1>
      <el-col :span="12" :offset="6">
      <el-form>
  
        <el-input type="" v-model="userId">
          <template slot="prepend">Username</template>
        </el-input>
           <el-input type="" v-model="password">
          <template slot="prepend">Password</template>
        </el-input>
        <el-button @click="onSubmitted">Login</el-button>
      </el-form>
      </el-col>
    </el-row>
</template>

<script>
export default {
}
</script>

<style>
h1{
    text-align: center
}
</style>
