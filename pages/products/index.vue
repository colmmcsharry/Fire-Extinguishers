<template lang="pug">
  .container
    LargeCardDisplay(v-for="cardInfo in largeCardInfo.slice(0,1)"
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