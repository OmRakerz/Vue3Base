<script>
export default {
  name: "App",
  data() {
    return {
      isAdmin: true,
    };
  },

  methods: {
    //Задание №1
    change: function () {
      this.isAdmin = !this.isAdmin;
    },
  },
};
</script>

<template>
  <h1>Упражнение №22</h1>
  <br />

  <!-- Задание №1 -->
  <h2>Задание №1</h2>
  <br />

  <p v-if="isAdmin">Текст1. Виден, когда isAdmin: true</p>
  <p v-else>Текст2. Виден, когда isAdmin: false</p>

  <br />
  <button @click="change()">Изменить значение</button>
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
