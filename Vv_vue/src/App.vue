<script>
export default {
  name: "App",
  data() {
    return {
      //Задание №1, №2
      newItem: "",
      items: ["a", "b", "c", "d", "e"],
    };
  },

  methods: {
    //Задание №1
    addFirstItem: function () {
      this.items.unshift(this.newItem);
    },
    //Задание №2
    addlastItem: function () {
      this.items.push(this.newItem);
    },
  },
};
</script>

<template>
  <h1>Упражнение №53</h1>
  <br />

  <!-- Задание №1 -->
  <h2>Задание №1</h2>
  <br />

  <ul class="ul">
    <li v-for="(item, index) in items" :key="index">
      {{ item }}
    </li>
  </ul>

  <!-- Задание №2 -->
  <h2>Задание №2</h2>

  <input class="input" v-model="newItem" />
  <button class="button" @click="addFirstItem">add first</button>
  <button class="button" @click="addlastItem">add last</button>

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
  font-size: 20px;
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
