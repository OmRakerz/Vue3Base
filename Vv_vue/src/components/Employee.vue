<script>
export default {
  props: { name: String, salary: String, age: Number },

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
  <p>Имя: {{ name }}</p>
  <p>Зарплата: {{ salary }}₽</p>
  <p>Возраст: {{ age }}</p>
</template>

<style></style>
