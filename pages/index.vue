<template lang="pug">
  .container
    Hero
    LargeCardDisplay(v-for="cardInfo in largeCardInfo"
    :key="cardInfo.id"
    :cardsSection="cardInfo")

    smallCardDisplay(v-for="cardInfo in smallCardSections"
    :key="cardInfo.id"
    :cardsSection="cardInfo")

</template>

<script>
import { largeCardSections, smallCardSections } from "@/assets/data.js"

export default {
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardSections: smallCardSections
    }
  }
}
</script>


<style scoped>

</style>