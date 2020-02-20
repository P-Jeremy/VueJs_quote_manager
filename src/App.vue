<template>
  <div class="container">
    <app-new-quote @newQuote="addQuote"></app-new-quote>
    <app-grid @deleteQuote="removeQuote" :quotes="quotes"></app-grid>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">
          Info: Click on a quote to delete it
        </div>
      </div>
    </div>
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
  },
  methods: {
    addQuote (txt) {
      this.quotes.push(txt)
    },
    removeQuote (index) {
      this.quotes.splice(index, 1)
    }
  }
}
</script>

<style>
</style>
