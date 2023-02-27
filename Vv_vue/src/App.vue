<script>
export default {
  name: "App",
  data() {
    return {
      //Задание №1, №2
      language: "",
      visible1: false,
      visible2: false,
      visible3: false,
    };
  },

  methods: {
    //Задание №1, №2
    choice1() {
      this.visible1 = true;
      this.visible2 = false;
      this.visible3 = false;
    },

    choice2() {
      this.visible2 = true;
      this.visible1 = false;
      this.visible3 = false;
    },

    choice3() {
      this.visible3 = true;
      this.visible1 = false;
      this.visible2 = false;
    },
  },
};
</script>

<template>
  <h1>Упражнение №48</h1>
  <br />

  <!-- Задание №1 -->
  <h2>Задание №1</h2>

  <p>Какой ваш родной язык?</p>
  <input
    name="radio"
    type="radio"
    v-model="language"
    value="Русский"
    @click="choice1"
  />
  <label for=""><span> Русский</span> </label>
  <br />

  <input
    name="radio"
    type="radio"
    v-model="language"
    value="Английский"
    @click="choice2"
  />
  <label for=""><span> Английский</span></label>
  <br />

  <input
    name="radio"
    type="radio"
    v-model="language"
    value="Казахский"
    @click="choice3"
  />
  <label for=""><span> Казахский</span></label>

  <!-- Задание №2 -->
  <h2>Задание №2</h2>

  <p v-if="visible1">Привет</p>
  <p v-if="visible2">Hello</p>
  <p v-if="visible3">ЖУМАЙСЫНБА</p>

  <p>Ваш национальный язык: {{ language }}</p>

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
  margin: 5px;
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

span {
  color: #00bfff;
  font-size: 20px;
}
</style>
