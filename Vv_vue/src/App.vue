<script>
export default {
  name: "App",
  data() {
    return {
      visible: true,
    };
  },

  methods: {
    //Задание №1
    button1: function () {
      this.visible = true;
    },
    button2: function () {
      this.visible = false;
    },
  },
};
</script>

<template>
  <h1>Упражнение №17</h1>
  <br />

  <div>
    <!-- Задание №1  -->
    <h2>Задание №1</h2>
    <p v-if="visible">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolor sequi
      excepturi dolores harum dignissimos cum.
    </p>

    <p v-if="!visible">
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Tenetur, illo!
      Cupiditate numquam, obcaecati adipisci, assumenda porro officiis
      doloremque architecto temporibus ratione veritatis fugit animi. Quae!
    </p>
    <br />
    <button @click="button1()">Показать первый абзац</button>
    <button @click="button2()">Показать второй абзац</button>
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
