<template>
    <div class="container">
        <my-header></my-header>
        <my-new-quote @quoteAdded="addNewQuote"></my-new-quote>
        <my-quotes :quotes="quotes"></my-quotes>
    </div>
</template>

<script>
    import Header from './components/Header.vue';
    import addQuote from './components/AddQuote.vue';
    import Quotes from './components/Quotes.vue';

    export default {
        data: function() {
            return {
                quotes: [],
                maxQuotes: 10,
            }
        },
        methods: {
            addNewQuote(quote) {
                this.quotes.push(quote);
            }
        },
        components: {
            myHeader: Header,
            myNewQuote: addQuote,
            myQuotes: Quotes,
        }
    }
</script>

<style>
</style>
