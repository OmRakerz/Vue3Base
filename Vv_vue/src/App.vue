<script>
export default {
  name: "App",
  data() {
    return {
      visible1: false,
      visible2: true,
    };
  },

  methods: {
    //Задание №1
    show1: function () {
      this.visible1 = true;
    },

    //Задание №2 и 3
    hide2: function () {
      this.visible2 = false;
    },
    show2: function () {
      this.visible2 = true;
    },
  },
};
</script>

<template>
  <h1>Упражнение №19</h1>
  <br />

  <!-- Задание №1 -->
  <h2>Задание №1</h2>
  <br />

  <p v-if="visible1">
    Lorem, ipsum dolor sit amet consectetur adipisicing elit. Itaque, ipsam
    exercitationem! Voluptates unde atque molestias similique eos laboriosam,
    minus laborum harum culpa quis voluptatum cupiditate.
  </p>
  <button class="link" @click="show1">Показать текст</button>

  <br />
  <br />

  <!-- Задание №2 -->
  <h2>Задание №2</h2>
  <br />

  <p v-if="visible2">
    Lorem ipsum dolor sit, amet consectetur adipisicing elit. Sapiente, dolorem
    animi quasi iure non asperiores eos. Nesciunt modi rem eveniet!
  </p>
  <button class="link" @click="show2">Показать текст</button>
  <button class="link" @click="hide2">Скрыть текст</button>

  <br />
  <br />

  <!-- Задание №3 -->
  <h2>Задание №3</h2>
  <br />

  <p v-if="visible2">
    Lorem ipsum, dolor sit amet consectetur adipisicing elit. Rerum minima nam
    unde, commodi repudiandae repellendus placeat eveniet facere nesciunt
    consequuntur veniam blanditiis possimus quaerat maxime.
  </p>
  <button class="link" @click="show2" v-if="!visible2">Показать текст</button>
  <button class="link" @click="hide2" v-if="visible2">Скрыть текст</button>

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
  width: 70%;
  color: white;
}
/* ---------------- */
a {
  font-family: sans-serif;
  font-size: 20px;
}
</style>
