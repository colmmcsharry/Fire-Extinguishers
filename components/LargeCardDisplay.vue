.<template lang="pug">
  .container 
    h4.header {{ cardsSection.title}}
    p.snippet {{cardsSection.snippet}}
    .cards-container
      LargeCard(v-for="card in cardsSection.cards"
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
    margin-top: 2rem;
}
    .header {
        font-weight: 700;
        font-size: 1.5rem;
    }
    .snippet {
        color: grey;
        margin-bottom: 1.5rem;
    }
    .cards-container {
        display: flex;
        justify-content: space-between;
    }
</style>