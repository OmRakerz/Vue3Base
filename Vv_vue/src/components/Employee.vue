<script>
export default {
  props: { id: Number, name: String, surn: String },
  emits: ["change"],

  data() {
    return {
      //Задание №1
      isEdit: false,
      newName: this.name,
      newSurn: this.surn,
    };
  },

  methods: {
    //Задание №1
    edit() {
      this.isEdit = true;
    },
    save() {
      this.isEdit = false;
      this.$emit("change", this.id, this.newName, this.newSurn);
    },
  },
};
</script>

<template>
  <!-- Задание №1 -->
  <template v-if="!isEdit">
    <p>Id: {{ id }}</p>
    <p>Имя: {{ name }}</p>
    <p>Фамилия: {{ surn }}</p>
    <button class="button" @click="edit">edit</button>
    <br />
    <br />
  </template>

  <template v-else>
    <input class="input" v-model="newName" />
    <input class="input" v-model="newSurn" />
    <button class="button" @click="save">save</button>
  </template>
</template>

<style></style>
