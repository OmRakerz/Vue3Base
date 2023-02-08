<script>
export default {
  name: "App",
};
</script>

<template>
  <h1>Задание №1</h1>
  <p>Hello, World!</p>
  <br />
  <p>I'm Valera</p>

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
</style>
