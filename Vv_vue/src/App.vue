<script>
export default {
  name: "App",
  data() {
    return {
      //Задание №1
      num: 5,

      //Задание №2
      num1: 1,
      num2: 2,
      num3: 3,
    };
  },
};
</script>

<template>
  <h1>Упражнение №6</h1>
  <br />

  <div>
    <!-- Задание №1  -->
    <p>Задание №1. Квадрат из числа 5 = {{ num ** 2 }}</p>

    <br />

    <!-- Задание №2 -->
    <p>Задание №2. Сумма чисел 1, 2, 3 равна {{ num1 + num2 + num3 }}</p>
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

p {
  font-size: 25px;
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
