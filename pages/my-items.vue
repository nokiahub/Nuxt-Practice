<template>
  <div class="container">{{ myRentals }}</div>
</template>

<script>
import { mapState } from "vuex";
export default {
  layout: "no-nav",
  computed: {
    ...mapState(["myRentals"])
  }
};
</script>

<style lang="scss" scoped>
</style>
