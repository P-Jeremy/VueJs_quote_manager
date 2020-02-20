<template>
  <div class="row">
    <app-quote
    v-for="(quote, index) in quotes"
    :key="quote"
    @click.native="deleteQuote(index)"
    :quote="quote"
    />
  </div>
</template>

<script>
import Quote from './Quote'
export default {
  props: ['quotes'],
  components: {
    appQuote: Quote
  },
  methods: {
    deleteQuote (index) {
      this.$emit('deleteQuote', index)
    }
  }
}
</script>

<style>
</style>
