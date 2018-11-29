<template>
  <section class="container">
    <div>
      {{ product.name }}
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style lang="sass">

.container
  min-height: 100vh
  display: flex
  justify-content: center
  align-items: center
  text-align: center

</style>
