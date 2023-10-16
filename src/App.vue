<script setup>
import { ref, reactive } from "vue";
import navbar from "./components/navbar.vue";

const imgURLArr = [
  `../public/img/pockmon1.jpg`,
  `../public/img/pockmon2.jpg`,
  `../public/img/pockmon3.jpg`,
  `../public/img/pockmon4.jpg`,
  `../public/img/pockmon5.jpg`,
  `../public/img/pockmon6.jpg`,
  `../public/img/pockmon7.jpg`,
  `../public/img/pockmon8.jpg`,
  `../public/img/pockmon9.jpg`,
  `../public/img/pockmon10.jpg`,
  `../public/img/pockmon11.jpg`,
  `../public/img/pockmon12.jpg`,
];

const displayWaterfallFlow = () => {};

window.addEventListener("load", () => {
  displayWaterfallFlow();
});
</script>

<template>
  <navbar />

  <!-- 瀑布流圖片 -->
  <div class="imgArea">
    <img
      class="pockmonImg"
      v-for="item in imgURLArr"
      :src="item"
      alt="神奇寶貝"
      title="神奇寶貝"
    />
  </div>

  <!-- ?icon -->
  <img src="../public/icon/question-icon.svg" class="icon" title="更多" />
</template>

<style scoped>
.imgArea {
  padding: 0 10%;
  /* 將欄位分成3等分 */
  column-count: 3;

  .pockmonImg {
    max-width: 100%;
    height: auto;
    margin: 0.5rem;
    border-radius: 8px;
  }
}

.icon {
  height: 4vw;
  width: 4vw;
  padding: 0.5rem;
  border-radius: 50%;
  /*水平偏移:0 垂直偏移:3px 模糊半徑:6px 擴散半徑:3px(數值為負，使陰影收縮到元素內部) 顏色:#777*/
  box-shadow: 0 3px 6px 3px #777;
  position: fixed;
  bottom: 1%;
  right: 1%;
}
</style>
