<template>
<div>
<el-form-item >
    <span slot="label">{{labels}}</span>
    <el-input v-if="controltype === 'input'" 
        v-bind="$attrs" 
        value="" 
        @input.native="$emit('input', $event.target.value)"/> 
</el-form-item>
<el-form-item>
    <el-input 
        v-if="controltype=== 'textarea'"
        placeholder="สัดส่วน บราๆ"
           v-bind="$attrs" 
        value="" 
        @input.native="$emit('input', $event.target.value)"/>
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
        }, 
        methods: {
      change(event) {
        console.log("The value is: " + event.target.value);
        //HERE I can't get "event.target"
      }
    }
    }
}
</script>

<style>
    
</style>