<template>
  <div class="black-bg" v-if="모달창열림">
    <div class="white-bg">
      <h4 @click="모달창열림 = false">상세페이지</h4>
      <p>상세페이지내용</p>
    </div>
  </div>

  <div class="menu">
    <a v-for="작명 in 메뉴들" :key="작명">{{ 작명 }}</a>
  </div>

  <div v-for="(방이름, i) in products" :key="i">
    <img :src="방이름.image" alt="Room Image" class="room-img" />
    <h4 @click="모달창열림 = true">{{ 방이름.title }}</h4>
    <p>{{ 방이름.price }}원</p>
  </div>
</template>

<script>
import data from "./assets/room.js";

export default {
  name: "App",
  data() {
    return {
      모달창열림: true,
      신고수: [0, 0, 0],
      메뉴들: ["Home", "About", "Contact"],
      products: data,
    };
  },
  methods: {
    incresse(i) {
      this.신고수[i] += 1;
    },
  },
  components: {},
};
</script>

<style>
body {
  margin: 0;
}
div {
  box-sizing: border-box;
}
.black-bg {
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  position: fixed;
  padding: 20px;
}
.white-bg {
  width: 100%;
  background: white;
  padding: 20px;
  border-radius: 10px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}

.menu a {
  color: white;
  padding: 10px;
}

.room-img {
  width: 300px;
  margin-top: 40px;
}
</style>
