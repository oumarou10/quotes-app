<template>
    <div class="row">
        <app-quote-show v-for="(quote, index) in quotes" @click.native="deleteQuote(index)">{{ quote }}</app-quote-show>
    </div>
</template>

<script>
    import QuoteShow from './QuoteShow.vue'

    export default {
        name: "quote",
        props: ['quotes'],
        components: {
            appQuoteShow: QuoteShow
        },
        methods: {
            deleteQuote(index) {
                this.$emit('quoteDeleted', index)
            }
        }
    }
</script>

<style scoped>

</style>