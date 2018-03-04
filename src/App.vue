<template>
  <div id="app">
    <img src="./assets/logo.png" width="80">
    <app-quote-grid :quote="quotes"></app-quote-grid>
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid'
export default {
  name: 'app',
  data () {
    return {
      quotes: [
        'Coding is coding no matter the language'
      ],
      maxQuotes: 10
    }
  },
  components: {
    appQuoteGrid: QuoteGrid
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
