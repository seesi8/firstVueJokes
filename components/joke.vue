<template>
  <nuxt-link :to="'jokes/' + id">
    <div class="joke">
      <p class="text">{{ joke }}</p>
    </div>
  </nuxt-link>
</template>

<script>
export default {
  name: "Joke",
  props: ["joke", "id"],
};
</script>

<style>
.joke {
  border: 0.15rem grey dashed;
  border-radius: 0.5rem;
  margin: 1vh 3vh 1vh 0vh;
  padding: 0vw 2vw;
  text-decoration: none;
}

.text {
  text-decoration: none;
}

p {
  font-size: large;
  color: #000;
  text-decoration: none;
  font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
}
</style>
