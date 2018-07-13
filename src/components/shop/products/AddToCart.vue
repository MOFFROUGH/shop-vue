<template>
  <button type="button" :class="product.inventory ? 'btn btn-primary' : ' btn btn-danger'"
    :disabled="!product.inventory"
    @click="addToCart(product)">
    {{text}}
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
  ]),
  computed: {
    text () {
      return this.product.inventory ? 'Add to cart' : 'Out of Stock'
    }
  }
}
</script>
