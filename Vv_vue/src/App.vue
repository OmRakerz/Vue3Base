<script>
export default {
  name: "App",
  data() {
    return {
      day: "Среда",
    };
  },

  methods: {
    //Задание №1
  },
};
</script>

<template>
  <h1>Упражнение №23</h1>
  <br />

  <!-- Задание №1 -->
  <h2>Задание №1</h2>
  <br />

  <p v-if="day === 'Понедельник'">Понедельник</p>
  <p v-if="day === 'Вторник'">Вторник</p>
  <p v-if="day === 'Среда'">Среда</p>
  <p v-if="day === 'Четверг'">Четверг</p>
  <p v-if="day === 'Пятница'">Пятница</p>
  <p v-if="day === 'Суббота'">Суббота</p>
  <p v-if="day === 'Воскресенье'">Воскресенье</p>
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
