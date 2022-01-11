.<template lang="pug">
  .card
    img.image(:src="require(`@/assets/images/${card.image || 'fe1.jpg'}`)" 
              :alt="card.title")
    h3.header {{card.title}}
    p.snippet {{card.snippet}}
</template>

<script>
export default {
props:['card']
}
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
    }
    .snippet {
        color: grey
    }
</style>