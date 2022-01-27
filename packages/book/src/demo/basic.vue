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
        'https://vkceyugu.cdn.bspapp.com/VKCEYUGU-efbfcb02-017d-4e68-a2c7-f92e33192dbb/936b5f5c-c28b-4332-8bf8-cb18ba2e9f2b.jpeg',
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
