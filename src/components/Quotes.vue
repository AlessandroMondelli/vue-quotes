<template>
    <div class="row">
        <my-quote v-for="(quote,index) in quotes" @click.native="deleteQuote(index)">{{ quote }}</my-quote>
    </div>
</template>

<script>
import Quote from './Quote.vue';

export default {
    props: ['quotes'],
    components: {
        myQuote: Quote,
    },
    methods: {
        deleteQuote(index) {
            this.$emit('quoteDeleted',index); //Invio indice frase da eliminare ad app.vue
        }
    }
}
</script>

<style>
    .row {
        margin-top: 45px;
    }
</style>