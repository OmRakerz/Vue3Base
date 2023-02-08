<script>
export default {
  name: "App",
  data() {
    return {};
  },

  methods: {
    //Задание №2
    oneclick: function () {
      alert("Первое и единственное нажатие на кнопку");
    },
  },
};
</script>

<template>
  <h1>Упражнение №16</h1>
  <br />

  <div>
    <h2>Задание №1</h2>
    <a
      class="link"
      href="https://code.mu/ru/javascript/framework/vue/book/prime/basis/events-modifiers/"
      onclick="event.preventDefault()"
      >Клик по этой ссылке не приводит к переходу по ней</a
    >

    <br />
    <h2>Задание №2</h2>
    <br />
    <p>Сработает только одно нажатие по кнопке</p>
    <button @click.once="oneclick()">Button</button>
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
  font-size: 20px;
}
</style>
