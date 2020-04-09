<template>
  <div class="home">
    <Button contentStyle="color:yellow;background-color:black" @btnClick="btnClick">aaaaa</Button>

    <div
      style="margin-top:10px;float:left;width:31%;margin-left:6px"
      v-for="item in bookList"
      :key="item.id"
    >
      <BookItem :bookData="item"></BookItem>
    </div>
  </div>
</template>

<script>
import Button from '@/components/button/index.vue'

import BookItem from '@/components/bookitem/index.vue'

export default {
  name: 'Home',
  components: { Button, BookItem },
  data() {
    return {
      bookList: [
        {
          id: 1,
          bookName: 'book1',
          author: 'zs'
        },
        {
          id: 2,
          bookName: 'book12',
          author: 'zs1'
        },
        {
          id: 3,
          bookName: 'book13',
          author: 'zs2'
        },
        {
          id: 4,
          bookName: 'book14',
          author: 'zs3'
        }
      ]
    }
  },
  methods: {
    btnClick() {
      console.log('在父组件内点击了按钮')
    }
  }
}
</script>
