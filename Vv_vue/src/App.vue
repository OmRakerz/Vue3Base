<script>
export default {
  name: "App",
  data() {
    return {
      //Задание №1
      obj: {
        hidden: true,
      },
    };
  },

  methods: {
    // Задание №2
    show: function () {
      this.obj.hidden = false;
    },
    // Задание №3
    hide: function () {
      this.obj.hidden = true;
    },
    // Задание №4
    toggle: function () {
      this.obj.hidden = !this.obj.hidden;
    },
  },
};
</script>

<template>
  <h1>Упражнение №39</h1>
  <br />

  <!-- Задание №1 -->
  <h2>Задание №1</h2>

  <p :class="obj">
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Odit asperiores
    dolores iure, rerum vero possimus pariatur provident, voluptatem earum,
    neque hic! Cum magni sit perferendis assumenda ipsum. Quos, doloribus
    distinctio!
  </p>
  <br />

  <h2>Задание №2</h2>
  <button @click="show">Показать</button>

  <h2>Задание №3</h2>
  <button @click="hide">Скрыть</button>
  <br />

  <h2>Задание №4</h2>
  <button @click="toggle">{{ obj.hidden ? "Показать" : "Скрыть" }}</button>

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

a {
  font-family: sans-serif;
  font-size: 20px;
}
/* ---------------- */

/* Задание №1 */
p.hidden {
  display: none;
}
</style>
