<template>
    <div class="container">
      <van-search
        v-model="value"
        placeholder="请输入搜索关键词"
        show-action
        shape="round"
        @search="onSearch"
      >
        <div slot="action" @click="onSearch">搜索</div>
      </van-search>
      <van-radio-group v-model="radio">
        <van-cell-group>
          <van-cell title="单选框 1" clickable @click="findman(1)">
            <van-radio slot="right-icon" name="1" />
          </van-cell>
          <van-cell title="单选框 2" clickable @click="findman(2)">
            <van-radio slot="right-icon" name="2" />
          </van-cell>
        </van-cell-group>
      </van-radio-group>
    </div>
</template>

<script>
export default {
  name: 'findman',
  data () {
    return {
      radio: ''
    }
  },
  methods: {
    findman (man) {
      this.radio = man
    }
  }
}
</script>

<style scoped>

</style>
