<template>
  <div class="container">
    <div class="title tac">书名:{{bookData.bookName}}</div>
    <div class="author tac">作者:{{bookData.author}}</div>
  </div>
</template>

<script>
export default {
  props: {
    bookData: {
      type: Object,
      default: () => {
        return {
          bookName: '',
          author: ''
        }
      }
    }
  }
}
</script>

<style lang="less" scoped>
@import url('./index');
</style>