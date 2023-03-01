<script>
export default {
  props: { id: Number, name: String, salary: Number, age: Number },

  data() {
    return {
      //Задание №1
    };
  },

  methods: {
    //Задание №1
  },
};
</script>

<template>
  <!-- Задание №1 -->
  <p>Работник №{{ id }}</p>

  <p>Имя: {{ name }}</p>

  <p>Зарплата: {{ salary }}₽</p>

  <p>Возраст: {{ age }}</p>
  <br />
  <br />
</template>

<style></style>
