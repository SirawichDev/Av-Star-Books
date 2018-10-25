<template>
    <el-row :gutter="10">
      <h1>Login Page</h1>
      <el-col :span="10" :offset="6">
        <Form/>
      </el-col>
    </el-row>
</template>

<script>
import Form from '@/components/login/login.vue';
export default {
  components: {
    Form
  }
}
</script>

<style scoped>
h1{
    text-align: center
}
</style>
