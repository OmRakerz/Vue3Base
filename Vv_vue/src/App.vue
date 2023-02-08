<script>
export default {
  name: "App",
  data() {
    return {
      cost: 45,
      amount: 5,
    };
  },

  computed: {
    price: function () {
      return this.cost * this.amount;
    },
  },

  methods: {
    //Задание №2
    newprice: function () {
      this.cost = this.cost + 15;
    },
  },
};
</script>

<template>
  <h1>Упражнение №15</h1>
  <br />

  <div>
    <!-- Задание №1  -->
    <h2>Задание №1</h2>
    <br />
    <p>Цена продукта: {{ cost }}</p>
    <p>Количество продуктов: {{ amount }}</p>
    <p>Полная стоимость продуктов: {{ price }}</p>

    <!-- Задание №2-->
    <h2>Задание №2</h2>
    <br />
    <p>Нажмите на кнопку, для изменения значения цены на 15</p>
    <button @click="newprice">Обновление цены</button>
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
  font-size: 25px;
}
</style>
