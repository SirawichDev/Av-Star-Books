<template>
    <el-form>
        <app-input control-type="input" labels="Email"
            />
             <app-input control-type="input" labels="Password"
            />
            <app-button type="submit">{{isLogin ? 'Login' : 'Sign Up'}}</app-button>
                  <app-button type="button" @click="isLogin = !isLogin">Switch to {{ isLogin ? 'Sign up' : 'Login'}}</app-button>
    </el-form>
</template>

<script>
import AppButton from '@/components/UI/Button.vue';
import AppInput from '@/components/UI/Input.vue';
export default {
    name: 'AdminAuth',
    components:{
        AppButton,
        AppInput
    },
    data(){
        return{
            isLogin: true
        }
    }
}
</script>

<style>

</style>

