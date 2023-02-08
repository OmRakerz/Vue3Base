<script>
export default {
  name: "App",
  data() {
    return {
      //Задание №1
      arr: ["x", "y", "z"],

      //Задание №2
      arr1: [1, 2, 3],
    };
  },
};
</script>

<template>
  <h1>Упражнение №7</h1>
  <br />

  <div>
    <!-- Задание №1  -->
    <h2>Задание №1</h2>
    <p>Первый элемент массива: {{ arr[0] }}</p>
    <br />
    <p>Второй элемент массива: {{ arr[1] }}</p>
    <br />
    <p>Третий элемент массива: {{ arr[2] }}</p>

    <br />

    <!-- Задание №2 -->
    <h2>Задание №2</h2>
    <p>Сумма элементов массива = {{ arr1[0] + arr1[1] + arr1[2] }}</p>
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
