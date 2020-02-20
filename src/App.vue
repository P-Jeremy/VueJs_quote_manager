<template>
  <div class="container">
  <app-header :maxQuotes="maxQuotes" :quoteCount="quotes.length"/>
    <app-new-quote @newQuote="addQuote"/>
    <app-grid @deleteQuote="removeQuote" :quotes="quotes"/>
    <div v-if="this.quotes.length" class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">Info: Click on a quote to delete it</div>
      </div>
    </div>
  </div>
</template>

<script>
import QuotesGrid from './components/QuoteGrid'
import NewQuote from './components/NewQuote'
import Header from './components/Header'

export default {
  components: {
    appGrid: QuotesGrid,
    appNewQuote: NewQuote,
    appHeader: Header
  },
  data () {
    return {
      maxQuotes: 10,
      quotes: ['Paris is always a good idea']
    }
  },

  methods: {
    addQuote (txt) {
      if (this.quotes.length >= this.maxQuotes) {
        return alert('Max quotes exceeded')
      }
      if (!txt) {
        return
      }
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
