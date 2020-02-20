<template>
  <div class="container">
    <app-new-quote @newQuote="quotes.push($event)"></app-new-quote>
    <app-grid :quotes="quotes"></app-grid>
  </div>
</template>

<script>
import QuotesGrid from './components/QuoteGrid'
import NewQuote from './components/NewQuote'
export default {
  components: {
    appGrid: QuotesGrid,
    appNewQuote: NewQuote
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
