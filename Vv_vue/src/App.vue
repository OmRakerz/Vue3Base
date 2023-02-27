<script>
export default {
  name: "App",
  data() {
    return {
      //Задание №1
      text1: "",

      //Задание №2
      text2: "",
      text_arr: "",
    };
  },

  methods: {
    //Задание №2
    split_text: function () {
      this.text_arr = this.text2.split(" ");
    },
  },
};
</script>

<template>
  <h1>Упражнение №45</h1>
  <br />

  <!-- Задание №1 -->
  <h2>Задание №1</h2>
  <br />

  <textarea v-model="text1"></textarea>
  <p>{{ text1 }}</p>
  <br />

  <!-- Задание №2 -->
  <h2>Задание №2</h2>
  <br />

  <textarea v-model="text2"></textarea>
  <button class="button" @click="split_text">Список</button>

  <ul class="ul">
    <li v-for="elem in text_arr">{{ elem }}</li>
  </ul>

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
  color: black;
  text-align: center;
  font-size: 30px;
  margin: 10px;
}
</style>
