<template>
  <span class="container" @click="btnClick" :style="getStyle()">
    <slot></slot>
  </span>
</template>

<script>
export default {
  props: {
    contentStyle: {
      type: String,
      default: ''
    }
  },
  created() {},
  methods: {
    btnClick() {
      this.$emit('btnClick')
    },

    // 更新按钮样式
    getStyle() {
      return this.contentStyle
    }
  }
}
</script>

<style lang="less" scoped>
@import url('./index');
</style>