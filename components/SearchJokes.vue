<template>
  <form @submit.prevent="onSubmit">
    <input
      @input="onSubmit"
      type="text"
      name=""
      id=""
      v-model="text"
      placeholder="Search Jokes..."
    />
  </form>
</template>

<script>
export default {
  name: "SearchJokes",
  data() {
    return {
      text: "",
    };
  },
  methods: {
    onSubmit() {
      this.$emit("search-text", this.text);
    },
  },
};
</script>

<style>
input {
  background-color: transparent;
  border: grey solid 0.2rem;
  border-radius: 0.5rem;
  height: 2vh;
  width: 20vw;
  margin: 1vh 0vh;
  padding: 0vh 1vw;
}
</style>
