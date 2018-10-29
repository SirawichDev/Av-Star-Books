<template>
<div>
<el-form-item >
    <span slot="label">{{labels}}</span>
    <el-input v-if="controltype === 'input'" 
        v-bind="$attrs" 
        :value="value" 
        @input="$emit('input', $event.target.value)"> 
    </el-input>
</el-form-item>
<el-form-item>
    <el-input 
        v-if="controltype=== 'textarea'"
        placeholder="ss"
        :value="value" 
        @input="$emit('input', $event.target.value)">
    </el-input>
</el-form-item>

</div>
</template>

<script>
export default {
    name: 'input',
    props:{
        controltype: {
            type: String,
            default: 'input'
        },
        value: {
            type: String,
            default: ''
        },
        labels: {
            type: String,
            default: ''
        }
    }
}
</script>

<style>
    
</style>