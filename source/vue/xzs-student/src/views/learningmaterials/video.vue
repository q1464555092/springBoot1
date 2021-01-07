<template>
    <el-row >
      <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" >
        <el-menu-item index="0">分类：</el-menu-item>
        <el-menu-item index="1">Java视频</el-menu-item>
        <el-menu-item index="2">JS大全</el-menu-item>
        <el-menu-item index="3" >消息队列</el-menu-item>
        <el-menu-item index="4"><a href="https://www.ele.me" target="_blank">订单管理</a></el-menu-item>
      </el-menu>
        <el-col :span="3" v-for="(o, index) in 4" :key="o" :offset="index > 0 ? 2 : 0">
          <el-card :body-style="{ left: '20px',top:'-20px' }">
            <img src="https://shadow.elemecdn.com/app/element/hamburger.9cf7b091-55e9-11e9-a976-7f4d0b07eef6.png" class="image">
            <div style="padding: 14px;">
              <span>好吃的汉堡</span>
              <div class="bottom clearfix">
                <time class="time">{{ currentDate }}</time>
                <el-button type="text" class="button">操作按钮</el-button>
              </div>
            </div>
          </el-card>
        </el-col>
      </el-row>
</template>
<script>
export default {

  name: 'video',
  data () {
    return {
      form: {
        name: '',
        region: '',
        date1: '',
        date2: '',
        delivery: false,
        type: [],
        resource: '',
        desc: ''
      },
      activeIndex: '1',
      activeIndex2: '1'

    }
  }
}
</script>

<style scoped>
  .el-menu--horizontal>.el-menu-item {
    left: 180px;
  }
</style>
