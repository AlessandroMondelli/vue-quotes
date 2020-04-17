<template>
    <div class="text-center">
        <h2>Quote</h2>
        <textarea v-model="quote" placeholder="Insert a quote" rows="4" cols="50"></textarea>
        <br>
        <button @click="addQuoteToArray()" class="btn btn-primary">Add Quote</button>
    </div>
</template>

<script>
export default {
    data: function() {
        return {
            quote: '',
            quotes: [],
        }
    },
    methods: {
        addQuoteToArray() {
            this.quotes.push(this.quote); //Inserisco quote in array
            this.quote = ''; //Svuoto text area
            console.log(this.quotes);
        }
    }
}
</script>

<style>
    h2 {
        margin-top: 50px;
        font-size: 18px;
        font-weight: bold;
    }

    .btn {
        margin-top: 10px;
        font-size: 14px;
        padding: 4px 10px;
    }
</style>