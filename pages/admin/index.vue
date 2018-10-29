<template>
<div>
    <el-row type="flex" justify="center">
        <el-header >
                <el-button @click="$router.push('/admin/new-post')">
                    Create Posts
                </el-button>

</el-header>
    </el-row>
    <post-builder/>
    </div>
</template>

<script>
import PostBuilder from '~/components/Post/buildList.vue';

export default {
    components:{
        PostBuilder
    }
}
</script>


<style scoped>

</style>
