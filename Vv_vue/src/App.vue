<script>
export default {
  name: "App",
  data() {
    return {
      //Задание №1, №2, №3, №4, №5, №6
    };
  },

  methods: {
    // Задание №1
  },
};
</script>

<template>
  <h1>Упражнение №36</h1>
  <br />

  <!-- Задание №1 -->
  <h2>Стилизация компонента в фреймворке Vue</h2>
  <br />

  <p>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde hic vel
    voluptatum reprehenderit. Accusamus nobis atque omnis, maiores earum dolor
    voluptatum unde numquam ut libero, ducimus commodi, nam provident nihil!
  </p>

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
