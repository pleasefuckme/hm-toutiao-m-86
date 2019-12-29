<template>
  <div class="container">
    <br>
    <van-cell-group>
      <van-cell style="height: 106px;" title="报修人" value="选择人员" />
      <van-cell style="height: 106px;" title="所在区域" value="选择区域" />
      <van-cell style="height: 106px;" title="所在单体" value="选择单体" />
      <van-cell style="height: 106px;" title="设备名称" value="选择设备" />
      <van-cell style="height: 106px;" title="设备编号" value="选择编号" />
      <van-cell style="height: 106px;" title="报修内容" value="请输入报修内容" />
      <van-cell style="height: 106px;" title="故障描述" value="请输入故障描述" />
      <van-cell title="故障描述" value="请输入故障描述" >
        <van-uploader v-model="fileList" multiple />
      </van-cell>
    </van-cell-group>
  </div>
</template>

<script>
export default {
  name: 'wantbx'
}
</script>

<style scoped>

</style>
