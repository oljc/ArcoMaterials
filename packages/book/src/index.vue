<template>
  <div class="book-wrapper">
    <div class="book-cover">
      <img v-if="src" class="book" :src="src" />
    </div>
    <div class="book-inside" :style="{ backgroundColor: insideBgColor }"></div>
    <div class="book-inside" :style="{ backgroundColor: insideBgColor }"></div>
    <div class="book-inside" :style="{ backgroundColor: insideBgColor }"></div>
    <div class="book-inside" :style="{ backgroundColor: insideBgColor }"></div>
    <div class="book-inside" :style="{ backgroundColor: insideBgColor }"></div>
    <div
      class="book-inside"
      :style="{ backgroundColor: insideBgColor }"
      @click="insideClick"
    >
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
};
</script>

<style lang="less">
.book-wrapper {
  .book-cover {
    width: 100%;
    height: 100%;
    background-color: var(--color-bg-1);
    .book {
      width: 100%;
      height: 100%;
    }
  }
  .book-inside {
    width: 96%;
    height: 100%;
    left: 0;
    border: 1px solid lightgray;
    background-color: var(--color-bg-2);
    color: var(--color-text-2);
    -moz-user-select: none;
    -webkit-user-select: none; /*webkit浏览器*/
    -ms-user-select: none; /*IE10*/
    -khtml-user-select: none; /*早期浏览器*/
    user-select: none;
  }
  .book-end {
    left: 0;
    top: 2%;
    border: 1px lightgray solid;
    background-color: var(--color-bg-1);
  }
}
.book-wrapper div {
  position: absolute;
  border-radius: 0 2px 2px 0;
  box-shadow: 0 1px 8px 10px rgba(212, 212, 212, 0.08);
}
.book-wrapper {
  -webkit-perspective: 800px;
  perspective: 800px;
  -webkit-transform-style: preserve-3d;
  transform-style: preserve-3d;
  transform: translate3d(0, 0, 0);
}
.book-wrapper div {
  -webkit-transform-origin: left;
  transform-origin: left;
  transform: translate3d(0, 0, 0);
}
/* nth-of-type(*)是选择器匹配同类型中的第n个同级兄弟元素-从1开始 */
/*鼠标离开页面回翻的旋转时间*/
.book-wrapper div:nth-of-type(1) {
  -webkit-transform: rotateY(0deg);
  transform: rotateY(0deg);
  -webkit-transition: 1s;
  transition: 1s;
}
.book-wrapper div:nth-of-type(2) {
  -webkit-transform: rotateY(5deg);
  transform: rotateY(5deg);
  -webkit-transition: 0.9s;
  transition: 0.9s;
}
.book-wrapper div:nth-of-type(3) {
  -webkit-transform: rotateY(10deg);
  transform: rotateY(10deg);
  -webkit-transition: 0.8s;
  transition: 0.8s;
}
.book-wrapper div:nth-of-type(4) {
  -webkit-transform: rotateY(15deg);
  transform: rotateY(15deg);
  -webkit-transition: 0.7s;
  transition: 0.7s;
}
.book-wrapper div:nth-of-type(5) {
  -webkit-transform: rotateY(20deg);
  transform: rotateY(20deg);
  -webkit-transition: 0.6s;
  transition: 0.6s;
}
.book-wrapper div:nth-of-type(6) {
  -webkit-transform: rotateY(25deg);
  transform: rotateY(25deg);
  -webkit-transition: 0.5s;
  transition: 0.5s;
}
.book-wrapper div:nth-of-type(7) {
  -webkit-transform: rotateY(25deg);
  transform: rotateY(25deg);
  -webkit-transition: 0.4s;
  transition: 0.4s;
}
.book-wrapper div:nth-of-type(8) {
  -webkit-transform: rotateY(30deg);
  transform: rotateY(30deg);
  -webkit-transition: 0.3s;
  transition: 0.3s;
}
/*鼠标悬停时的旋转角度和旋转时间*/
.book-wrapper:hover div:nth-of-type(1) {
  -webkit-transform: rotateY(-160deg);
  transform: rotateY(-160deg);
  -webkit-transition: 1s;
  transition: 1s;
}
.book-wrapper:hover div:nth-of-type(2) {
  -webkit-transform: rotateY(-155deg);
  transform: rotateY(-155deg);
  -webkit-transition: 1.2s;
  transition: 1.2s;
}
.book-wrapper:hover div:nth-of-type(3) {
  -webkit-transform: rotateY(-145deg);
  transform: rotateY(-145deg);
  -webkit-transition: 1.5s;
  transition: 1.5s;
}
.book-wrapper:hover div:nth-of-type(4) {
  -webkit-transform: rotateY(-138deg);
  transform: rotateY(-138deg);
  -webkit-transition: 1.7s;
  transition: 1.7s;
}
.book-wrapper:hover div:nth-of-type(5) {
  -webkit-transform: rotateY(-132deg);
  transform: rotateY(-132deg);
  -webkit-transition: 1.8s;
  transition: 1.8s;
}
.book-wrapper:hover div:nth-of-type(6) {
  -webkit-transform: rotateY(-125deg);
  transform: rotateY(-125deg);
  -webkit-transition: 1.8s;
  transition: 1.8s;
}
.book-wrapper:hover div:nth-of-type(7) {
  -webkit-transform: rotateY(0deg);
  transform: rotateY(0deg);
  -webkit-transition: 1.85s;
  transition: 1.85s;
}
.book-wrapper:hover div:nth-of-type(8) {
  -webkit-transform: rotateY(-1deg);
  transform: rotateY(-1deg);
  -webkit-transition: 1.9s;
  transition: 1.9s;
}
</style>
