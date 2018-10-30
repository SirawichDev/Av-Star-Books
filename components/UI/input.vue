<template>
<div>
<el-form-item >
    <span slot="label">{{labels}}</span>
    <input v-if="controltype === 'input'" 
        v-bind="$attrs" 
        :value="value" 
        @input="$emit('input', $event.target.value)"/> 
</el-form-item>
<el-form-item>
    <input 
        v-if="controltype=== 'textarea'"
        placeholder="สัดส่วน บราๆ"
           v-bind="$attrs" 
        :value="value" 
        @input="$emit('input', $event.target.value)"/>
</el-form-item>

</div>
</template>

<script>
export default {
    name: 'inputs',
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