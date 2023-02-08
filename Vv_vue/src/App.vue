<script>
export default {
  name: "App",
  data() {
    return {
      date: 3,
    };
  },

  methods: {
    // Задание №1
    getDate: function () {
      let week = [
        "Понедельник",
        "Вторник",
        "Среда",
        "Четверг",
        "Пятница",
        "Суббота",
        "Воскресенье",
      ];
      return week[this.date - 1];
    },

    // Задание №2
    showDay: function () {
      let day = this.getDate(this.date);
      alert(day);
    },
  },
};
</script>

<template>
  <h1>Упражнение №12</h1>
  <br />

  <div>
    <!-- Задание №1 и №2  -->
    <h2>Задание №1 и №2</h2>
    {{ showDay() }}
    <br />
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
