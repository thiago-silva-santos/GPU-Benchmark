<template>
  <div>
    <input type="text" v-model="text" @keyup="submit" />
  </div>
</template>

<script>
export default {
  emits: ["inputEvent"],
  props: {
    input: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      text: '',
    };
  },
  methods: {
    submit() {
      this.$emit("inputEvent", this.text);
    },
  },
};
</script>

<style>
</style>