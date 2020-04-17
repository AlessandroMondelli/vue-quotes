<template>
    <div class="row">
        <my-quote v-for="quote in quotes">{{ quote }}</my-quote>
    </div>
</template>

<script>
import Quote from './Quote.vue';

export default {
    props: ['quotes'],
    components: {
        myQuote: Quote,
    }

}
</script>

<style>
    .row {
        margin-top: 45px;
    }
</style>