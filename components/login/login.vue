<template>
    <el-form>
        <el-input type="" >
          <template slot="prepend">Username</template>
        </el-input>
        <div class="line"></div>
        <el-input type="">
          <template slot="prepend">Password</template>
        </el-input>
        <el-button class="center" >Login</el-button>
    </el-form>
</template>

<script>
export default {
    
}
</script>

<style>
    .center{

        flex-direction: row;
        justify-content: center;

    }
</style>
