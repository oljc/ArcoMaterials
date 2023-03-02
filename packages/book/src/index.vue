<template v-once>
  <div class="book-wrapper">
    <div class="book-cover">
      <img v-if="src" class="book" :src="src" />
    </div>
    <div v-for="i in 5" :key="i" class="book-inside" :style="insideStyle"></div>
    <div class="book-inside" :style="insideStyle" @click="insideClick">
      <slot></slot>
    </div>
    <div class="book-end"></div>
  </div>
</template>

<script lang="ts">
export default {
  name: 'Book',
  components: {},
  props: {
    /**
     * 图片地址
     */
    src: String,
    /**
     * 书本内部点击事件回调
     */
    insideClick: {
      type: Function,
    },
    /**
     * 内页颜色
     */
    insideBgColor: {
      type: String,
      default: '#fff',
    },
  },
  computed: {
    insideStyle() {
      return { backgroundColor: this.insideBgColor };
    },
  },
};
</script>
