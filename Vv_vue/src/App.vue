<script>
export default {
  name: "App",
  data() {
    return {
      //Задание №1, №2, №3, №4, №5, №6
      arr: ["a", "b", "c", "d", "e", "f"],
    };
  },

  methods: {
    // Задание №1
    add: function () {
      this.arr.push("g");
    },
    // Задание №2
    delf: function () {
      this.arr.shift();
    },
    // Задание №3
    dell: function () {
      this.arr.pop();
    },
    // Задание №4
    splice: function () {
      this.arr.splice(2, 1);
    },
    // Задание №5
    sort: function () {
      this.arr.sort();
    },
    // Задание №6
    reverse: function () {
      this.arr.reverse();
    },
  },
};
</script>

<template>
  <h1>Упражнение №35</h1>
  <br />

  <!-- Задание №1 -->
  <h2>Задания №1, №2, №3, №4, №5, №6</h2>
  <br />

  <!-- Задание №1 -->
  <ul class="ul">
    <li v-for="elem in arr">{{ elem }}</li>
  </ul>
  <button @click="add">add</button>

  <!-- Задание №2 -->
  <button @click="delf">del first</button>

  <!-- Задание №3 -->
  <button @click="dell">del last</button>

  <!-- Задание №4 -->
  <button @click="splice">del penult</button>

  <!-- Задание №5 -->
  <button @click="sort">sort</button>

  <!-- Задание №6 -->
  <button @click="reverse">reverse order</button>

  <main>
    <TheWelcome />
  </main>
</template>

<style>
/* Стиль упражнений */
body {
  background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
    url(../background.png);
  background-position: 0 0;
  background-repeat: no-repeat;
  background-size: cover;
  font-family: sans-serif;
  background-attachment: fixed;
}

h1 {
  text-transform: uppercase;
  text-align: center;
  margin-top: 50px;
  font-size: 50px;
  color: #4682b4;
}

h2 {
  margin-top: 30px;
  font-size: 35px;
  color: #008080;
}

p {
  font-size: 25px;
  display: block;
  width: 70%;
  color: white;
}

.ul {
  color: #00bfff;
  font-size: 20px;
}
/* ---------------- */
a {
  font-family: sans-serif;
  font-size: 20px;
}
</style>
