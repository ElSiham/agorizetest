<template>
  <section class="container">
    <div
      v-for="product in products"
      :key="product.id"
      class="product"
    >
      <img
        :src="product.img"
        alt="product-img"
      >
      <div class="product-title">
        <span>{{ product.name }}</span>
        <span class="product-price"> {{ product.price }} € </span>
      </div>
      <div class="product-descr"> {{ product.descr }} </div>
      <button class="buy">
        add to cart
      </button>
    </div>
  </section>
</template>

<script>
import axios from 'axios'

export default {
  // components: {
  // },
  data () {
    return {
      products: []
    }
  },
  asyncData ({ params }) {
    return axios.get(`http://localhost:3003/products`)
    .then((res) => {
      console.log('coucou', res.data)
      // res.data.playlists.map(item => {
      //   item.size = item.size.toString()
      // })
      return {
        products: res.data
      }
    })
  }
}
</script>

<style lang="sass">

.container
  min-height: 100vh
  padding: 3rem
  .product
    position: relative
    height: 18rem
    border: 1px solid rgba(200, 200, 200, 1)
    border-radius: 3px
    margin-top: 1rem
    padding: 1rem
    img
      max-width: 100%
      max-height: 100%
    .product-title
      color: rgba(40, 40, 40, 1)
      margin: 1rem 0
      text-align: center
      font-weight: bold
      font-size: 1.3rem
      .product-price
        position: absolute
        right: 2rem
        top: 2rem
        font-size: 1rem
        background-color: rgba(240, 240, 240, 1)
        padding: .3rem
        border-radius: 3px
        color: rgba(0, 137, 123, 1)
    .product-descr
      color: rgba(104, 104, 104, 1)
      text-align: center
    .buy
      display: block
      margin: 1rem 0
      padding: .5rem
      border: none
      border-radius: 3px
      width: 100%
      background-color: rgba(191, 54, 12, 1)
      color: rgba(240, 240, 240, 1)
</style>
