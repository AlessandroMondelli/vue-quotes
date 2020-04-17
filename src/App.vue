<template>
    <div class="container">
        <my-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></my-header>
        <my-new-quote @quoteAdded="addNewQuote"></my-new-quote>
        <my-quotes :quotes="quotes" @quoteDeleted="deleteQuote"></my-quotes>
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
                if(quote.length > 0) {
                    if(this.quotes.length < 10) {
                        this.quotes.push(quote); //Inserisco frase
                    } else {
                        alert("Hai raggiunto il numero massimo di frasi, Clicca su una frase per eliminarla")
                    }
                } else {
                    alert("Non hai scritto nulla, riprova")
                }
            },
            deleteQuote(index) {
                this.quotes.splice(index,1); //Elimino frase a click
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
