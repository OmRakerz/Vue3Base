<script>
export default {
  props: ["arg"],

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

  <ul class="ul">
    <li v-for="elem in arg">{{ elem }}</li>
  </ul>
</template>

<style></style>
