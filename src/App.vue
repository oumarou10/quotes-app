<template>
    <div class="container">
        <app-header :quote-count="quotes.length" :maxQuotes="maxQuotes"></app-header>
        <app-quote-add @quoteWasAdded="newQuote"></app-quote-add>
        <app-quote :quotes="quotes" @quoteDeleted="deleteQuote"></app-quote>
        <div class="row">
            <div class="col-sm-12">
                <p class="alert alert-info text-center"> To delete a quote click on it</p>
            </div>
        </div>
    </div>
</template>

<script>
    import Quote from './components/Quote.vue'
    import QuoteAdd from './components/QuoteAdd.vue'
    import Header from './components/Header.vue'

    export default {
        components: {
          appQuoteAdd: QuoteAdd,
          appQuote: Quote,
          appHeader: Header
        },
        data: function () {
            return {
                maxQuotes: 10,
                quotes: [
                    'Just a simple quote'
                ]
            }
        },
        methods: {
            newQuote(quote) {
                this.quotes.push(quote)
            },
            deleteQuote(index) {
                this.quotes.slice(index, 1)
            }
        },
    }
</script>

<style>
</style>
