<template>
  <div>
    <h1>Home</h1>
    <p v-if="$fetchState.pending">Fetching Planets...</p>
    <p v-else-if="$fetchState.error">Error ...</p>
    <ul v-else>
      <li v-for="(planet, i) in planets" :key="i.slug">
        <NuxtLink :to="planet.slug">
          {{ planet.title }}
        </NuxtLink>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  async fetch() {
    this.planets = await fetch("https://api.nuxtjs.dev/planets").then((res) =>
      res.json()
    );
  },
  data() {
    return {
      planets: [],
    };
  },
};
</script>
