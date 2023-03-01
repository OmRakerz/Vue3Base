<script>
export default {
  props: { id: Number, name: String, surn: String },
  emits: ["remove"],

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
  <p>Id: {{ id }}</p>
  <p>Имя: {{ name }}</p>

  <p>Фамилия: {{ surn }}</p>

  <button class="button" @click="$emit('remove', id)">remove</button>
  <br />
  <br />
</template>

<style></style>
