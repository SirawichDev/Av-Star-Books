<template>
    <el-button :class="btnStyle" v-bind="$attrs" v-on="$listeners">
        <slot/>
    </el-button>
</template>

<script>
export default {
    name: 'Button',
    props: {
        btnStyle: {
            type: String,
            default: ''
        }
    }
}
</script>

<style>

</style>
