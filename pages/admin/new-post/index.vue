<template >

   <el-form @submit.prevent="onSave">

       <input-u-i control-type="input" v-model="editedPost.star_name" labels="star name "/>
       <input-u-i control-type="input" v-model="editedPost.title" labels="Title"/>
       <input-u-i v-model="editedPost.image" labels="Image Url"/>
        <input-u-i controltype="textarea" v-model="editedPost.content" labels="Content"/>
          <el-row type="flex" justify="center">
         <el-rate
    v-model="star"
    :colors="['#99A9BF', '#F7BA2A', '#FF9900']">
  </el-rate>
  </el-row>
        <button-u-i type="submit">Save</button-u-i>
        <el-button type="danger" plain @click="onCancel">Cancel</el-button>
        
</el-form>

</template>

<script>
import InputUI from '@/components/UI/input.vue';
import ButtonUI from '@/components/UI/Button.vue';
export default {
    components: {
        InputUI,
        ButtonUI
    },
    data(){
        return{
            editedPost:{
                star_name: '',
                title: '',
                image: '',
                content: ''
            },
            star: null
        }
    },
    methods:{
        onSave(){
            console.log(this.editedPost);
        },
        onCancel(){
            this.$router.push('/admin');
        }
    }
}
</script>

