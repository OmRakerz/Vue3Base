<script>
export default {
  name: "App",
  data() {
    return {};
  },

  methods: {
    show: function () {
      var data = new Date();
      alert(data.toDateString());
    },
  },
};
</script>

<template>
  <h1>Упражнение №10</h1>
  <br />

  <div>
    <!-- Задание №1  -->
    <h2>Задание №1</h2>
    {{ show() }}
    <p>Кликни</p>
    <button @click="show">Текущая дата</button>

    <br />
    <!-- Задание №2  -->
    <h2>Задание №2</h2>
    <p>Наведи</p>
    <button @mouseenter="show">Текущая дата</button>
  </div>
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
  margin-top: 25px;
  font-size: 35px;
  color: #008080;
}

p {
  font-size: 20px;
  display: block;
  width: 50%;
  color: white;
}
/* ---------------- */
a {
  font-family: sans-serif;
  font-size: 25px;
}
</style>
