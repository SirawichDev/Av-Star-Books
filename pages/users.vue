<template>
    <el-row :gutter="20">
      <el-col :span="12" :offset="6">
        <h1>Search Page</h1>
      <el-form>
        <el-input  v-model="userId"></el-input>
        <el-button @click="onLoadId">Show UID</el-button>
      </el-form>
        <nuxt-child/>
      </el-col>
    </el-row>
</template>
<script>
export default {
        data(){
      return {
        userId:''
      }
    },
    methods: {
      onLoadId(){
        this.$router.push('/users/'+ this.userId);
      }
    },
    layout: 'users'  //user layout 

}
</script>

