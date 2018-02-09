<template>
    <div class="container">
        <app-quote-add @quoteWasAdded="newQuote"></app-quote-add>
        <app-quote :quotes="quotes"></app-quote>
    </div>
</template>

<script>
    import Quote from './components/Quote.vue'
    import QuoteAdd from './components/QuoteAdd.vue'

    export default {
        components: {
          appQuoteAdd: QuoteAdd,
          appQuote: Quote,
        },
        methods: {
          newQuote(quote) {
              this.quotes.push(quote)
          }
        },
        data: function () {
            return {
                maxQuotes: 10,
                quotes: [
                    'Just a simple quote'
                ]
            }
        }
    }
</script>

<style>
</style>
