<template lang="pug">
  nav.navbar.navbar-expand-lg.navbar-dark.bg-dark.padding
    NuxtLink.navbar-brand(to="/") Firengii
    button.navbar-toggler(type='button' data-toggle='collapse' data-target='#navbarSupportedContent' aria-controls='navbarSupportedContent' aria-expanded='false' aria-label='Toggle navigation')
      span.navbar-toggler-icon
    #navbarSupportedContent.collapse.navbar-collapse.ml-auto
      ul.navbar-nav.ml-auto
        li.nav-item.active
          NuxtLink.nav-link(to="/products")  Products
            span.sr-only (current) 
        li.nav-item.active
          NuxtLink.nav-link(to="/my-items") My Items 
            span.sr-only (current)
</template>

<script>
export default {

}
</script>

<style scoped>
   .padding {
        padding: 1.5rem;
        background-color: black
    }
    .nav-left {
        margin-left: auto;
    }
</style>