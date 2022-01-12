<template lang="pug">
bigcontainer
  .container.py-5(v-if='product') 
    .hero-container
      img.image(:src='require(`@/assets/images/${product.image}`)' alt='')
      .info-box
        h1 {{ product.title }}
        p.snippet {{ product.snippet }}
        rentmodal(:product='product')
    .whats-included-container
      .included-container
        h6 Super Effective
        p Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores, dolorem.
      .included-container
        h6 Clean &amp; Tidy
        p Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores, dolorem.
      .included-container
        h6 Cancel Anytime
        p Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores, dolorem.
      .included-container
        h6 Satisfaction Guaranteed
        p Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores, dolorem.
    .description-container
      p
        | {{ product.description }}
    reviews
  .container.padding(v-else='')
    PageNotFound
</template>

<script>
export default {
  computed: {
    product() {
      return this.$store.getters.getProductById(this.$route.params.id);
    },
  },
};
</script>

<style scoped>
  .hero-container {
        display: flex;
        justify-content: space-between;
    }
    .image {
        width: 59%;
        height: 25rem;
    }
    .info-box {
        width: 39%;
        background-color: rgba(207, 201, 201, 0.322);
        padding: 1rem;
        border-radius: 0.5rem;
    }
    .whats-included-container {
        border-bottom: 0.1rem solid rgba(128, 128, 128, 0.151);
    }
    .description-container {
        border-bottom: 0.1rem solid rgba(128, 128, 128, 0.151);
        padding-bottom: 2rem;
        margin-bottom: 2rem;
    }
    .included-container {
        margin-top: 1.5rem;
    }
    h1 {
        font-size: 1.75rem;
    }
    h6 {
        font-size: 1.15rem;
        font-weight: 400;
    }
    p {
        color: grey
    }
    .snippet {
        color: rgba(0, 0, 0, 0.774);
        margin-top: 1rem;
    }
    button {
        width: 100%;
        border: none;
        padding: 0.5rem;
        color: white;
        font-weight: 700;
        padding: 1rem 4rem;
        border-radius: 100rem;
        background-color: rgb(231, 81, 43);
        color: white;
        font-weight: 700;
        transition: 0.5s;
    }
    .description-container {
        margin-top: 3rem;
        color: grey
    }
    .padding {
        padding: 1.5rem
    }


</style>
