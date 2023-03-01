<script>
export default {
  data() {
    return {
      newName: " ",
      newSurn: " ",
    };
  },
  methods: {
    save() {
      this.$emit("add", this.newName, this.newSurn);
    },
  },
};
</script>

<template>
  <input class="input" v-model="newName" />
  <input class="input" v-model="newSurn" />
  <button class="button" @click="save">Save</button>
</template>
