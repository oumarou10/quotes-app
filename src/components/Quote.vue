<template>
    <div class="row">
        <app-quote-show v-for="quote in quotes">{{ quote }}</app-quote-show>
    </div>
</template>

<script>
    import QuoteShow from './QuoteShow.vue'

    export default {
        name: "quote",
        props: ['quotes'],
        components: {
            appQuoteShow: QuoteShow
        }
    }
</script>

<style scoped>

</style>