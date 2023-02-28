<script>
export default {
  name: "App",
  data() {
    return {
      //Задание №1
      users: [
        {
          id: 1,
          name: "name1",
          salary: 100,
          age: 30,
        },
        {
          id: 2,
          name: "name2",
          salary: 200,
          age: 40,
        },
        {
          id: 3,
          name: "name3",
          salary: 300,
          age: 50,
        },
      ],
    };
  },

  methods: {
    //Задание №1
    removeItem: function (id) {
      this.users = this.users.filter((user) => {
        return user.id !== id;
      });
    },
  },
};
</script>

<template>
  <h1>Упражнение №55</h1>
  <br />

  <!-- Задание №1 -->
  <h2>Задание №1</h2>
  <br />

  <table>
    <tr>
      <th>Id</th>
      <th>Name</th>
      <th>Salary</th>
      <th>Age</th>
      <th>Remove</th>
    </tr>
    <tr v-for="user in users">
      <td>{{ user.id }}</td>
      <td>{{ user.name }}</td>
      <td>{{ user.salary }}</td>
      <td>{{ user.age }}</td>
      <td>
        <button class="button" @click="removeItem(user.id)">remove</button>
      </td>
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
  margin-left: 10px;
  font-size: 35px;
  color: #008080;
}

p {
  font-size: 25px;
  display: block;
  width: 70%;
  color: white;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  margin: 10px;
}

.ul {
  color: #00bfff;
  font-size: 20px;
}

a {
  font-family: sans-serif;
  font-size: 20px;
  margin-left: 10px;
}
/* ---------------- */

.button {
  color: #4682b4;
  text-align: center;
  font-size: 20px;
  margin: 4px 0;
  border-radius: 40px;
}

span {
  color: #00bfff;
  font-size: 20px;
}

.input {
  color: black;
  font-size: 20px;
  margin: 10px;
}

table {
  color: #4682b4;
  border: 1px solid white;
  margin: 10px;
  font-size: 20px;
}

td,
th {
  border: 2px solid white;
  padding: 5px;
}
</style>
