<template>
        <el-card>
      <img src="https://i.pinimg.com/originals/42/6c/39/426c39f797dba2caa9960ad931437e97.jpg" class="image" :height="40">
      <div style="padding: 14px;">
        <span>miew</span>
        <div class="bottom clearfix">
          <time class="time">{{ currentDate }}</time>
             <nuxt-link :to="'asian/' + 1">
          <el-button type="text" class="button">More Detail</el-button>
          </nuxt-link>
        </div>
      </div>
    </el-card>
</template>

<style scoped>
.image{
    height: 50%;
    padding: 20;
}
</style>
