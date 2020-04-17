<template>
    <div id="header">
        <h1>Quotes Added</h1>
        <div class="progress quotes-bar">
            <div class="progress-bar inner-bar" role="progressbar" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100" :style="{width: (quoteCount / maxQuotes) * 100 + '%'}">
                {{ quoteCount }} / {{ maxQuotes }}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['quoteCount','maxQuotes'],
}
</script>

<style>
    #header {
        padding: 20px 0;
    }

    .quotes-bar {
        height: 30px;
        border-radius: 3px;
        border: 1px solid rgb(117, 117, 117);
        width: 100%;
        background-color: white
    }

    .inner-bar {
        transition: 0.3s;
        width: 0%;
        height: 28px;
        background-color: #0069D9
    }
</style>
