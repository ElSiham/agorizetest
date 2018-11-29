<template>
  <div>
    <div class="header">
      <div class="shopname">My shop</div>
      <div class="navigation-links">
        <div class="link">Produits</div>
        <div class="link">Panier</div>
      </div>
    </div>
    <nuxt/>
  </div>
</template>

<style lang="sass">
body
  margin: 0
  padding: 0
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif
  font-size: 16px
  word-spacing: 1px
  background-color: #CDD3D5
  
  .header
    background-color: #506C64
    color: #CDD3D5
    .shopname
      float: left
      max-width: 50%
      padding: 1rem
      font-size: 2rem
      font-weight: bold
      color: #220C10
    .navigation-links
      display: flex
      justify-content: flex-end
      .link
        padding: 1rem

</style>
