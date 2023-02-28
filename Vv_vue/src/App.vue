<script>
export default {
  name: "App",
  data() {
    return {
      //Задание №1, №2
      isDisabled: true,
      isDisabled1: true,
      checked: false,
    };
  },

  methods: {
    //Задание №1, №2
    toggle: function () {
      this.isDisabled = false;
    },

    toggle1: function () {
      this.isDisabled1 = false;
    },
  },
};
</script>

<template>
  <h1>Упражнение №51</h1>
  <br />

  <!-- Задание №1 -->
  <h2>Задание №1</h2>
  <br />
  <input v-bind:disabled="isDisabled" />
  <br />
  <button class="button" @click="toggle">button</button>
  <br />

  <!-- Задание №2 -->
  <h2>Задание №2</h2>
  <input type="text" v-bind:disabled="isDisabled1" />
  <br />

  <input type="checkbox" v-model="checked" @click="toggle1" />

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
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  margin: 10px;
}

.ul {
  color: #00bfff;
  font-size: 20px;
}

a {
  font-family: sans-serif;
  font-size: 20px;
}
/* ---------------- */

.button {
  color: #4682b4;
  text-align: center;
  font-size: 15px;
  margin: 10px;
}

span {
  color: #00bfff;
  font-size: 20px;
}
</style>
