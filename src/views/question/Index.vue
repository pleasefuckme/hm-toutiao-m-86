<template>
  <div class='container'>
<!--    <div class="body-container" style="height: 100%" @scroll="scrollEvent">-->
    <el-scrollbar>
    <div style="height: 1140px">
      <div class="box-card" v-for="o in 10" :key="o">
        <br>
        <el-card class="box-card">
          <div slot="header">
            <div style="float: right; padding: 3px 0;color:#999999; font-size: 23px" type="text">12:24:00</div>
            <span style="color: #1a1a1a; font-size: 31px;font-family: 'PingFang SC'"><b>工单状态更新提醒</b></span><br><br>
            <span style="color: #333333; font-size: 27px;font-family: 'PingFang SC'">你有新的任务待领取</span><br><br>
          <div style=" line-height: 12px; color: #333333; font-size: 27px;font-family: 'PingFang SC'" v-for="o in 3" :key="o" class="text item">
            {{'我裂开了'}}
          </div>
          </div>
          <div class="clearfix">
            <router-link to="/findman" style="color: blue">详情</router-link>
<!--            <el-button style="float: left; padding: 3px 0" type="text">详情</el-button>-->
          </div>
        </el-card>
      </div>
    </div>
    </el-scrollbar>
  </div>
</template>

<script>
export default {
  name: 'question-index'
}
</script>

<style scoped lang='less'>
  .van-skeleton {
    margin-top: 10px;
  }
</style>
<style>
  .text {
    font-size: 14px;
    font-family: "PingFang SC";
  }

  .item {
    margin-bottom: 18px;
  }

  .clearfix:before,
  .clearfix:after {
    display: table;
    content: "";
  }

  .clearfix:after {
    clear: both
  }

  .box-card {
    width: 380px;
  }
</style>
