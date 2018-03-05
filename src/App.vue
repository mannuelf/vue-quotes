<template>
  <div id="app" class="container">
    <app-quote-grid :quote="quotes"></app-quote-grid>
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue'
import NewQuote from './components/NewQuote.vue'
import Header from './components/Header.vue'

export default {
  name: 'app',
  data () {
    return {
      quotes: [
        'Coding is coding no matter the language',
        'Tomorrow is another day'
      ],
      maxQuotes: 10
    }
  },
  methods: {
    newQuote(quote) {
      if (this.quotes.length >= this.maxQuotes) {
        return alert('please delete Quotes first')
      }
      this.quotes.push(quote)
    }
  },
  components: {
    appQuoteGrid: QuoteGrid,
    appNewQuote: NewQuote,
    appHeader: Header
  },
  created () {
    console.log('app init');
  }
}
</script>

<style>
@import url('https://cdnjs.cloudflare.com/ajax/libs/bulma/0.6.2/css/bulma.css');
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
