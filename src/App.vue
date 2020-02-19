<template>
  <div class="container">
    <app-grid :quotes="quotes"></app-grid>
  </div>
</template>

<script>
import quotesGrid from './components/QuoteGrid'
export default {
  components: {
    appGrid: quotesGrid
  },
  data () {
    return {
      maxQuotes: 10,
      quotes: [
        'Paris is always a good idea'
      ]
    }
  }
}
</script>

<style>
</style>
