<template>
 <el-menu class="el-menu-demo" mode="horizontal">
  <el-menu-item class="index" index="1">Home</el-menu-item>
  <el-submenu index="2">
    <template class="index" slot="title">Repo</template>
    <el-menu-item index="2-1">Japan</el-menu-item>
    <el-menu-item index="2-2">Korea</el-menu-item>
    <el-menu-item index="2-3">Russia</el-menu-item>
  </el-submenu>
  <el-menu-item index="3" disabled>Watch movie</el-menu-item>
  <el-menu-item index="4">
    <a >Login</a>
  </el-menu-item>
</el-menu>
</template>

<script>
export default {
  data: function() {
return {
    logged: true,
    notlogged: false
  };
},
};
</script>

 <style scoped>
 .index a.nuxt-link-active {
   color: green;

 }
 .el-menu-demo{
   background-color: snow;
 }
.el-row {
    margin-bottom: 20px;
  }
  .el-col {
    border-radius: 4px;
  }
  .bg-purple-dark {
    background: #99a9bf;
  }
  .bg-purple {
    background: #d3dce6;
  }
  .bg-purple-light {
    background: #e5e9f2;
  }
  .grid-content {
    border-radius: 4px;
    min-height: 36px;
  }
  .row-bg {
    padding: 10px 0;
    background-color: #f9fafc;
  }
</style>
