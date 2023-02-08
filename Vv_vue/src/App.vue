<script>
export default {
  name: "App",
  data() {
    return {
      //Задание №1
      obj: { x: 1, y: 2, z: 3 },
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
    <br />
    <p>Сумма элементов объекта obj = {{ obj.x + obj.y + obj.z }}</p>
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
