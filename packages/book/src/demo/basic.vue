<template>
  <Book class="test" :src="demoUrl" :inside-click="demoClick">
    <sonslot>
      <span>{{ text }}</span>
    </sonslot>
  </Book>
</template>

<script lang="ts">
import Book from 'arco-vue-book';

export default {
  name: 'BasicDemo',
  components: {
    Book,
  },
  data() {
    return {
      num: 0,
      text: '内页自定义内容',
      demoUrl:
        'https://img-blog.csdnimg.cn/50dc93e785354bc4b4ddf82915e78875.png',
    };
  },
  methods: {
    demoClick() {
      this.num++;
      this.text = `内页点击事件${this.num}`;
    },
  },
};
</script>
<style lang="less">
.test {
  width: 100px;
  height: 140px;
  margin: 20px auto;
}
</style>
