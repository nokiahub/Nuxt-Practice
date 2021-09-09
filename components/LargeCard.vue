<template>
  <!-- <NuxtLink :to="`/products/${card.id}`" class="card">
    <img :src="require(`@/assets/images/${card.image || 'fe1.jpeg'}`)" alt class="image" />
    <h3 class="header">{{card.title}}</h3>
    <p class="snippet">{{card.snippet}}</p>
  </NuxtLink> -->
  <div @click="handleRedirect" class="card">
    <img :src="require(`@/assets/images/${card.image || 'fe1.jpeg'}`)" alt class="image" />
    <h3 class="header">{{card.title}}</h3>
    <p class="snippet">{{card.snippet}}</p>
  </div>
</template>

<script>
export default {
  props: ["card"],
  methods: {
    handleRedirect() {
      this.$router.push({ name: "item", params: { id: this.card.id}})
    }
  }
};
</script>

<style scoped>
.card {
  width: 31.5%;
  height: 25rem;
  border: none;
  overflow: hidden;
  padding: 0;
  cursor: pointer;
}
.image {
  height: 65%;
  border-radius: 0.5rem;
}
.header {
  font-size: 1.15rem;
  margin-top: 0.4rem;
  color: black;
}
.header:hover {
  color: black;
  text-decoration: none;
}
.snippet {
  color: grey;
}
</style>
