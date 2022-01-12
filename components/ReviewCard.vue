
   
<template lang="pug">
    div.review-card
        div.image-container
            img(:src="review.picture.large" alt="")
        
        div.text-container
            h6 {{review.login.username}}
            p Lorem ipsum dolor, sit amet consectetur adipisicing elit. Repellendus quam magni beatae possimus debitis.
</template>

<script>
    export default {
        props: ['review'],
    }
</script>

<style scoped>
    .review-card {
        margin-top: 1.5rem;
        height: 4rem;
        display: flex;
    }
    .text-container {
        margin-left: 2rem
    }
    img {
        width: 4rem;
        height: 4rem;
        border-radius: 100%;
    }
    p {
        color: grey
    }
</style>