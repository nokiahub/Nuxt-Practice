<template>
  <div>
    <img :src="require(`@/assets/images/${card.image || 'fe1.jpeg'}`)" alt class="image" />
  </div>
</template>

<script>
export default {
  props: ["card"]
};
</script>

<style lang="scss" scoped>
</style>
