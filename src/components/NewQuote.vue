<template>
  <div class="row">
    <form action>
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-offset-3">
        <label for="quoteInput">Quote</label>
        <textarea class="form-control" name id="quoteInput" rows="3" v-model="quote"></textarea>
      </div>
      <div class="col-sm_8 col-sm-offset-2 col-xs-12 col-md-offset-3">
        <button class="btn btn-primary" @click.prevent="createNew">Add quote</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data () {
    return {
      quote: ''
    }
  },
  methods: {
    createNew () {
      this.$emit('newQuote', this.quote)
      this.quote = ''
    }
  }
}
</script>

<style>
</style>
