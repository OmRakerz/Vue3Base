<script>
export default {
  name: "App",
  data() {
    return {
      //Задание №1, №2
      items: [1, 2, 3],
    };
  },

  methods: {
    // Задание №1
    hrefs: [
      { href: "1.html", text: "text1" },
      { href: "2.html", text: "text2" },
      { href: "3.html", text: "text3" },
    ],

    // Задание №2
    products: [
      {
        name: "product1",
        price: 100,
        quantity: 5,
      },
      {
        name: "product2",
        price: 200,
        quantity: 4,
      },
      {
        name: "product3",
        price: 300,
        quantity: 3,
      },
    ],
  },
};
</script>

<template>
  <h1>Упражнение №31</h1>
  <br />

  <!-- Задание №1 -->
  <h2>Задание №1</h2>
  <br />

  <ul class="ul">
    <li v-for="elem in hrefs">
      <a href="{{ elem.href }}">{{ elem.text }}</a>
    </li>
  </ul>

  <!-- Задание №2 -->
  <h2>Задание №2</h2>
  <br />

  <table>
    <tr v-for="product in products">
      <td>{{ product.name }}</td>
      <td>{{ product.price }}</td>
      <td>{{ product.quantity }}</td>
    </tr>
  </table>
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
