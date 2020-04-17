<template>
    <div class="container">
        <my-header></my-header>
        <my-quote></my-quote>
        <my-quotes></my-quotes>
    </div>
</template>

<script>
    import Header from './components/Header.vue';
    import addQuote from './components/AddQuote.vue';
    import Quotes from './components/Quotes.vue';

    export default {
        components: {
            myHeader: Header,
            myQuote: addQuote,
            myQuotes: Quotes,
        }
    }
</script>

<style>
</style>
