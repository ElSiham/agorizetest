<template>
  <div>
    <div class="header">
      <div class="shopname">My shop</div>
      <div class="navigation-links">
        <div class="link-container">
          <a
            class="links"
            href="./product"
          >
            Products
          </a>
        </div>
        <div class="link-container">
          <a
            class="links"
            href=""
          >
            Cart (0)
          </a>
        </div>
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
  background-color: rgba(240, 240, 240, 1)
  
  .header
    // background-color: #F0F0EC
    .shopname
      float: left
      max-width: 50%
      padding: 1rem
      font-size: 2rem
      font-weight: bold
      color: rgba(40, 40, 40, 1)
    .navigation-links
      display: flex
      justify-content: flex-end
      .link-container
        padding: 1rem
        .links
          color: rgba(104, 104, 104, 1)
          text-decoration: none

</style>
