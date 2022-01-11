<template lang="pug">
  .container 
    h3.header {{ cardsSection.title}}
    .card-container
      SmallCard(v-for="card in cardsSection.cards"
                :key="card.id"
                :card="card")
  
</template>

<script>
export default {
  props: [
    'cardsSection'
  ]

}
</script>

<style scoped>

  .container {
        padding: 2rem 0
    }
    .header {
        font-weight: 700;
        font-size: 1.5rem;
        margin-bottom: 2rem;
    }
    .card-container {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
    }
</style>