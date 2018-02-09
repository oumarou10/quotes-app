<template>
    <div class="container">
        <app-quote :quotes="quotes"></app-quote>
    </div>
</template>

<script>
    import Quote from './components/Quote.vue'

    export default {
        components: {
          appQuote: Quote
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
