<script>
export default {
  name: "App",
  data() {
    return {
      visible1: true,
      visible2: true,
      visible3: true,
    };
  },

  methods: {
    //Задание №1
    toggle1: function () {
      this.visible1 = !this.visible1;
    },

    toggle2: function () {
      this.visible2 = !this.visible2;
    },

    toggle3: function () {
      this.visible3 = !this.visible3;
    },
  },
};
</script>

<template>
  <h1>Упражнение №21</h1>
  <br />

  <!-- Задание №1 -->
  <h2>Задание №1</h2>
  <br />

  <p>
    {{ visible1 ? "Скрыть первый абзац" : "Показать первый абзац" }}
  </p>
  <button @click="toggle1">Кнопка 1</button>

  <br />
  <br />
  <br />

  <p>
    {{ visible2 ? "Скрыть второй абзац" : "Показать второй абзац" }}
  </p>
  <button @click="toggle2">Кнопка 2</button>

  <br />
  <br />
  <br />

  <p>
    {{ visible3 ? "Скрыть третий абзац" : "Показать третий абзац" }}
  </p>
  <button @click="toggle3">Кнопка 3</button>
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
  font-size: 20px;
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
