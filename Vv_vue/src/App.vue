<script>
export default {
  name: "App",
  data() {
    return {
      //Задание №1
      arr: ["x", "y", "z"],
    };
  },

  methods: {
    //Задание №1
  },
};
</script>

<template>
  <h1>Упражнение №28</h1>
  <br />

  <!-- Задание №1 -->
  <h2>Задание №1</h2>
  <br />

  <ul class="ul" v-for="(elem, key) in arr">
    <li>{{ key }} {{ elem }}</li>
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

.p {
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
