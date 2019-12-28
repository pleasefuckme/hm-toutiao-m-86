<template>
  <div class='container'>
    <!--    <van-panel title="工作状态更新提醒" desc="你有新的工单任务待领取">-->
<!--      <div>-->
<!--      </div>-->
<!--&lt;!&ndash;      <div slot="footer">&ndash;&gt;-->
<!--&lt;!&ndash;        <van-button size="small">开</van-button>&ndash;&gt;-->
<!--&lt;!&ndash;        <van-button size="small" type="danger">关</van-button>&ndash;&gt;-->
<!--&lt;!&ndash;      </div>&ndash;&gt;-->
<!--    </van-panel>-->
    <div class="box-card" v-for="o in 3" :key="o">
    <br>
      <el-card class="box-card">
        <div slot="header" class="clearfix" >
          <div  style="float: right; padding: 3px 0;color:#999999; font-size: 23px" type="text">12:24:00</div>
          <span style="color: #1a1a1a; font-size: 31px;font-family: 'PingFang SC'"><b>工单状态更新提醒</b></span><br><br>
          <span style="color: #333333; font-size: 27px;font-family: 'PingFang SC'">你有新的任务待领取</span><br>
        </div>
        <div style="color: #333333; font-size: 27px;font-family: 'PingFang SC'" v-for="o in 3" :key="o" class="text item">
          {{'列表内容 ' + o }}
        </div>
        <hr style="width: 1334px ; color: #333333">
        <div class="clearfix">
          <el-button style="float: left; padding: 3px 0" type="text">详情</el-button>
        </div>
      </el-card>
    </div>
  </div>
</template>

<script>
export default {
  name: 'question-index'
}
</script>

<style scoped lang='less'>
.van-skeleton{
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
