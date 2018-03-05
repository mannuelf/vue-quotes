<template>
    <div class="row">
        <Quote v-for="quote in quotes" :key="quote.id"></Quote>
    </div>
</template>

<script>
    import Quote from './Quote.vue'

    export default {
        name: 'QuoteGrid',
        props: ['quotes'],
        components: {
            Quote
        },
        methods: {
            deleteQuote(index) {
                this.$emit('quoteDeleted', index);
            }
        },
        created () {
            console.log('QuoteGrid Init')
        }
    }
</script>

<style>

</style>