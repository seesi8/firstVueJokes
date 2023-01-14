<template>
  <header class="header">
    <h1 class="title">Jokes</h1>

    <ul>
      <li>
        <nuxt-link class="link" to="/">Home</nuxt-link>
      </li>
      <li>
        <nuxt-link class="link" to="/jokes">Jokes</nuxt-link>
      </li>
      <li>
        <nuxt-link class="link" to="/about">About</nuxt-link>
      </li>
    </ul>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
};
</script>

<style>
.title {
  font-family: "Courier New", Courier, monospace;
  color: rgb(40, 37, 37);
}
.header {
  display: flex;
  align-items: center;
  justify-content: space-around;
  background-color: rgb(201, 183, 183);
}

ul {
  list-style-type: none;
  white-space: nowrap;
  flex-wrap: nowrap;
}

li {
  display: inline;
  border-radius: 0.5rem;
  padding: 0.5rem;
  margin-right: 2vw;
  font-size: 2vh;
  background-color: rgb(205, 211, 197);
}

.link {
  color: black;
  font-weight: bold;
  text-decoration: none;
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
}
</style>
