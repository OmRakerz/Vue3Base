<script>
export default {
  name: "App",
  data() {
    return {
      visible: true,
    };
  },

  methods: {
    //Задание №1
    toggle: function () {
      this.visible = !this.visible;
    },
  },
};
</script>

<template>
  <h1>Упражнение №26</h1>
  <br />

  <!-- Задание №1 -->
  <h2>Задание №1</h2>

  <p v-show="visible">Абзац 1. Текст. Текст. Текст.</p>
  <br />

  <button @click="toggle">{{ visible ? "Скрыть" : "Показать" }}</button>

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
/* ---------------- */
a {
  font-family: sans-serif;
  font-size: 20px;
}
</style>
