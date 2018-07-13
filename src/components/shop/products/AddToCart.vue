<template>
<<<<<<< HEAD
  <button type="button" :class="product.inventory?'btn btn-primary':' btn btn-danger'"
    :disabled="!product.inventory"
    @click="addToCart(product)">
    {{text}}
=======
  <button type="button" class="btn btn-primary"
    :disabled="!product.inventory"
    @click="addToCart(product)">
    Add to cart
>>>>>>> origin/master
  </button>
</template>

<script>
import { mapActions } from 'vuex'

export default {
  name: 'AddToCart',
  props: {
    product: Object
  },
  methods: mapActions([
    'addToCart'
<<<<<<< HEAD
  ]),
  computed : {
    text () {
      return this.product.inventory?'Add to cart':'Out of Stock'
    }
  }
=======
  ])
>>>>>>> origin/master
}
</script>
