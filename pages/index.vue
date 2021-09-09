<template>
  <div class="container">
    <div class="">test</div>
    <Hero />
    <LargeCardDisplay
      v-for="cardInfo in largeCardInfo"
      :key="cardInfo.id"
      :cardsSection="cardInfo"
    />
    <SmallCardDisplay v-for="cardInfo in smallCardInfo" :key="cardInfo.id" :cardSection="cardInfo" />
  </div>
</template>

<script>
import { largeCardSections } from "@/assets/data.js";
import { smallCardSections } from "@/assets/data.js";
export default {
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections
    };
  }
};
</script>
