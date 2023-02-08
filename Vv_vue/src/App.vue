<script>
export default {
  name: "App",
  data() {
    return {};
  },

  methods: {
    // Задание №1 и №2
    numsquare: function (num) {
      alert(num ** 2);
    },
  },
};
</script>

<template>
  <h1>Упражнение №13</h1>
  <br />

  <div>
    <!-- Задание №1  -->
    <h2>Задание №1</h2>
    <br />
    <p>Нажми на кнопку, чтобы получить число 2 в квадрате</p>
    <button @click="numsquare(2)">2^2</button>

    <!-- Задание №2  -->
    <h2>Задание №2</h2>
    <br />
    <p>Нажми на кнопку, чтобы получить число 3 в квадрате</p>
    <button @click="numsquare(3)">3^2</button>
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
  margin-top: 30px;
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
