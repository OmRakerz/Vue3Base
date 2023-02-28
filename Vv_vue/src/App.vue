<script>
export default {
  name: "App",
  data() {
    return {
      //Задание №1, №2, №3
      text: "",
      enterPress: "",
      ctrlPress: "",
      mouse: "",
    };
  },

  methods: {
    //Задание №1, №2, №3
    submit: function () {
      this.enterPress = this.text;
    },

    ctrl: function () {
      this.ctrlPress = "Вы нажали на ссылку с зажатым ctrl";
    },

    left: function () {
      this.mouse = "left";
    },

    right: function () {
      this.mouse = "right";
    },

    middle: function () {
      this.mouse = "middle";
    },
  },
};
</script>

<template>
  <h1>Упражнение №52</h1>
  <br />

  <!-- Задание №1 -->
  <h2>Задание №1</h2>

  <p>Введите текст, а затем нажмите Enter</p>
  <input class="input" v-on:keypress.enter="submit" v-model="text" />
  <p>{{ enterPress }}</p>

  <!-- Задание №2 -->
  <h2>Задание №2</h2>

  <p>Нажмите на ссылку, зажав ctrl</p>
  <a href="#" @click.ctrl="ctrl">link</a>
  <p>{{ ctrlPress }}</p>

  <!-- Задание №3 -->
  <h2>Задание №3</h2>

  <p>Нажмите на ссылку левой, правой, а также средней кнопкой мыши</p>
  <a href="#" @click.left="left" @click.right="right" @click.middle="middle"
    >link</a
  >
  <p>{{ mouse }}</p>

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
  margin-left: 10px;
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
  margin-left: 10px;
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

.input {
  color: black;
  font-size: 20px;
  margin: 10px;
}
</style>
