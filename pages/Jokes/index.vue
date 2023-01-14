<template>
  <div class="jokes">
    <SearchJokes v-on:search-text="searchText" />

    <Joke
      v-for="joke in jokes"
      :key="joke.id"
      :id="joke.id"
      :joke="joke.joke"
    />
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      jokes: [],
    };
  },
  async created() {
    const config = {
      headers: {
        Accept: "application/json",
      },
    };
    try {
      const res = await axios.get("https://icanhazdadjoke.com/search", config);
      this.jokes = res.data.results;
    } catch (error) {}
  },

  head() {
    return {
      title: "Dad Jokes",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "best place for corny dad jokes",
        },
      ],
    };
  },
  methods: {
    async searchText(text) {
      const config = {
        headers: {
          Accept: "application/json",
        },
      };
      try {
        const res = await axios.get(
          `https://icanhazdadjoke.com/search?term=${text}`,
          config
        );
        this.jokes = res.data.results;
      } catch (error) {}
    },
  },
};
</script>

<style>
.jokes {
  margin-left: 2vw;
}
</style>
