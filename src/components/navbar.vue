<script setup>
import { ref } from "vue";
</script>

<template>
  <div class="navbar">
    <img src="../../public/icon/house-icon.svg" class="h-icon" />
    <span class="home">首頁</span>
    <div class="bluid">
      <span class="addtext">建立</span>
      <img src="../../public/icon/arror-down-icon.svg" class="l-icon" />
    </div>
    <div class="serachBox">
      <img src="../../public/icon/search-icon.svg" class="l-icon" />
      <input type="text" placeholder="搜尋" class="searchBar" />
    </div>
    <img src="../../public/icon/bell-icon.svg" class="icon" />
    <img src="../../public/icon/message-icon.svg" class="icon" />
    <img src="../../public/icon/arror-down-icon.svg" class="icon" />
  </div>
</template>

<style scoped>
.h-icon {
  height: 4vw;
  width: 4vw;
}
.icon {
  height: 4vw;
  width: 4vw;
  border-radius: 50%;
  padding: 0.5rem;
  transition: all 0.3s ease;

  &:hover {
    background-color: #c0c0c0;
    cursor: pointer;
  }
}

.l-icon {
  height: 2vw;
  width: 2vw;
}
.navbar {
  height: 15vh;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 1rem;

  .home {
    padding: 0.5rem 1rem;
    border-radius: 20px;
    background-color: black;
    color: white;
    font-size: 1.5rem;
    font-weight: bold;
    transition: all 0.5s ease;

    &:hover {
      background-color: #c0c0c0;
      color: black;
      cursor: pointer;
    }
  }

  .bluid {
    display: flex;
    align-items: center;
    padding: 0.5rem 1rem;
    border-radius: 20px;
    transition: all 0.5s ease;

    &:hover {
      background-color: #777;
      color: white;
      cursor: pointer;
    }

    .addtext {
      font-size: 1.5rem;
      font-weight: bold;
    }
    .icon {
      margin-left: 0.5rem;
    }
  }

  .serachBox {
    display: flex;
    position: relative;
    .l-icon {
      position: absolute;
      top: 25%;
      left: 3%;
    }
    .searchBar {
      width: 30rem;
      height: 3rem;
      background-color: rgb(219, 219, 219);
      border: none;
      border-radius: 20px;
      font-size: 1.35rem;
      padding-left: 3rem;
    }
  }
}
</style>
