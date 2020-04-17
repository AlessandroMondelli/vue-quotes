<template>
    <div id="header">
        <h1>Quotes Added</h1>
        <div id="quotes-bar">
            <div id="inner-bar"></div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style>
    #header {
        padding: 20px 0;
    }

    #quotes-bar {
        height: 30px;
        border-radius: 3px;
        border: 1px solid rgb(117, 117, 117);
        width: 100%;
        background-color: white
    }

    #inner-bar {
        transition: 0.3s;
        width: 10%;
        height: 28px;
        background-color: #0069D9
    }
</style>
