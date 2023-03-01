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
    showApp1: function () {
      this.$emit("show1", "xxx");
    },

    showApp2: function () {
      this.$emit("show2", "yyy");
    },
  },
};
</script>

<template>
  <!-- Задание №1 -->
  <button class="button" @click="showApp1">One func</button>
  <button class="button" @click="showApp2">Two func</button>
</template>

<style></style>
