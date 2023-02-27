<script>
export default {
  name: "App",
  data() {
    return {
      //Задание №1
      num1: 0,
      square_num1: 0,

      //Задание №2
      num2: 0,
      num3: 0,
      sum_num23: "",

      //Задание №3
      text1: 0,
      text2: 0,
      swapt1_t2: "Смена значений",

      //Задание №4
      fullName: "",
      Name: "",
      Surname: "",
      Patronymic: "",
    };
  },

  methods: {
    //Задание №1
    square: function () {
      this.square_num1 = this.num1 ** 2;
    },

    //Задание №2
    sum: function () {
      this.sum_num23 = Number(this.num2) + Number(this.num3);
    },

    //Задание №3
    swap: function () {
      const x = this.text1;
      this.text1 = this.text2;
      this.text2 = x;
    },

    //Задание №4
    split: function () {
      this.Surname = this.fullName.split(" ")[0];
      this.Name = this.fullName.split(" ")[1];
      this.Patronymic = this.fullName.split(" ")[2];
    },
  },
};
</script>

<template>
  <h1>Упражнение №44</h1>
  <br />

  <!-- Задание №1 -->
  <h2>Задание №1</h2>
  <br />
  <input type="num1" v-model="num1" />
  <button @click="square">Square</button>
  <p>Квадрат числа {{ num1 }} равен: {{ square_num1 }}</p>

  <!-- Задание №2 -->
  <h2>Задание №2</h2>
  <br />

  <input type="num2" v-model="num2" />
  <input type="num3" v-model="num3" />
  <button @click="sum">Sum</button>
  <br />
  <p>Сложение чисел {{ num2 }} и {{ num3 }} равна: {{ sum_num23 }}</p>
  <br />

  <!-- Задание №3 -->
  <h2>Задание №3</h2>
  <br />
  <input type="text" v-model="text1" />
  <input type="text" v-model="text2" />
  <button @click="swap">Swap</button>
  <br />
  <p>{{ swapt1_t2 }}</p>
  <br />

  <!-- Задание №4 -->
  <h2>Задание №4</h2>
  <br />

  <input type="text" v-model="fullName" />
  <button @click="split">Split ФИО</button>
  <p>Фамилия: {{ Surname }}</p>
  <p>Имя: {{ Name }}</p>
  <p>Отчество: {{ Patronymic }}</p>

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
</style>
