<template>
    <div class="text-center">
        <h2>Quote</h2>
        <form>
            <textarea v-model="quote" placeholder="Insert a quote" rows="4" cols="50"></textarea>
            <br>
            <button @click.prevent="newQuote()" class="btn btn-primary">Add Quote</button>
        </form>
    </div>
</template>

<script>
export default {
    data: function() {
        return {
            quote: '',
        }
    },
    methods: {
        newQuote() {
            this.$emit('quoteAdded', this.quote)
            this.quote = ''; //Svuoto text area
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