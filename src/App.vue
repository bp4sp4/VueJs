<template>
  <Modal />

  <div class="menu">
    <a v-for="menu in 메뉴들" :key="menu">{{ menu }}</a>
  </div>

  <Discount />

  <div v-for="(rooms, i) in 원룸들" :key="i">
    <img :src="원룸들[i].image" class="room-img" />
    <h4
      @click="
        모달창열렸니 = true;
        누른거 = i;
      "
    >
      {{ 원룸들[i].title }}
    </h4>
    <p>{{ 원룸들[i].price }}원</p>
  </div>
</template>

<script>
import data from "./assets/oneroom.js";
import Discount from "./Discount.vue";
import Modal from "./Modal.vue";

export default {
  name: "App",
  data() {
    return {
      누른거: 0,
      원룸들: data,
      모달창열렸니: false,
      메뉴들: ["HOME", "Shop", "About"],
    };
  },

  methods: {
    increase() {
      this.신고수 += 1;
    },
  },
  components: {
    Discount: Discount,
    Modal: Modal,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.body {
  margin: 0;
}

div {
  box-sizing: border-box;
}

.discount {
  background: #eee;
  padding: 20px;
  margin: 10px;
  border-radius: 5px;
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
  border-radius: 8px;
  padding: 20px;
}

.room-img {
  width: 100%;
  margin-top: 40px;
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
</style>
