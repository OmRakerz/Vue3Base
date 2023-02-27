<script>
export default {
  name: "App",
  data() {
    return {
      //Задание №1, №2, №3
      selected1: "",
      selected2: "",
      selected3: "",

      dayWeek: "",
      dayWeekOptions: [
        "Понедельник",
        "Вторник",
        "Среда",
        "Четверг",
        "Пятница",
        "Суббота",
        "Воскресенье",
      ],

      day: "",
      dayOptions: [
        "1",
        "2",
        "3",
        "4",
        "5",
        "6",
        "7",
        "8",
        "9",
        "10",
        "11",
        "12",
        "13",
        "14",
        "15",
        "16",
        "17",
        "18",
        "19",
        "20",
        "21",
        "22",
        "23",
        "24",
        "25",
        "26",
        "27",
        "28",
        "29",
        "30",
        " 31",
      ],

      month: "",
      monthOptions: [
        "Январь",
        "Февраль",
        "Март",
        "Апрель",
        "Май",
        "Июнь",
        "Июль",
        "Август",
        "Сентябрь",
        "Октябрь",
        "Ноябрь",
        "Декабрь",
      ],

      year: "",
      yearOptions: [
        "2023",
        "2022",
        "2021",
        "2020",
        "2019",
        "2018",
        "2017",
        "2016",
        "2015",
        "2014",
        "2013",
        "2012",
        "2011",
        "2010",
        "2009",
        "2008",
        "2007",
        "2006",
        "2005",
        "2004",
        "2003",
      ],
    };
  },

  methods: {
    //Задание №3
    todayDate: function () {
      var today = new Date();
      this.day = String(today.getDate());
      this.month = String(today.getMonth() + 1);
      this.year = today.getFullYear();
    },
  },
};
</script>

<template>
  <h1>Упражнение №50</h1>
  <br />

  <!-- Задание №1 -->
  <h2>Задание №1</h2>

  <select v-model="dayWeek">
    <option v-for="option in dayWeekOptions">{{ option }}</option>
  </select>
  <br />
  <!-- Задание №2 -->
  <h2>Задание №2</h2>

  <select v-model="selected1">
    <option v-for="option in dayOptions">{{ option }}</option>
  </select>
  <select v-model="selected2">
    <option v-for="option in monthOptions">{{ option }}</option>
  </select>
  <select v-model="selected3">
    <option v-for="option in yearOptions">{{ option }}</option>
  </select>

  <br />
  <!-- Задание №3 -->
  <h2>Задание №3</h2>

  <select v-model="day">
    <option>{{ day }}</option>
  </select>
  <select v-model="month">
    <option>{{ month }}</option>
  </select>
  <select v-model="year">
    <option>{{ year }}</option>
  </select>

  <button class="button" @click="todayDate">Today's date</button>

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
  margin: 10px;
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
  color: #4682b4;
  text-align: center;
  font-size: 15px;
  margin: 10px;
}

span {
  color: #00bfff;
  font-size: 20px;
}
</style>
