<script>
export default {
  props: { show1: String, show2: String },

  data() {
    return {
      //Задание №1
    };
  },

  methods: {
    //Задание №1
    func1: function () {
      this.$emit("show1", "Valera");
    },

    func2: function () {
      this.$emit("show2", "Evgeniy", "5000₽");
    },
  },
};
</script>

<template>
  <!-- Задание №1 -->
  <button class="button" @click="func1">Имя</button>
  <button class="button" @click="func2">Имя/ЗП</button>
</template>

<style></style>
