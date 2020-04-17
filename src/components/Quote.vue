<template>
    <div class="col-lg-3 col-md-3 col-sm-6">
        <div class="panel panel-default">
            <div class="panel-body quote">
                <slot></slot>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style>
    .panel-body {
        font-family: 'Great Vibes', cursive;
        font-weight: bold;
        font-size: 24px;
    }

    .quote {
        cursor: pointer;
        transition: 0.2s;
    }

    .quote:hover {
        background-color: rgba(219, 101, 101, 0.171);
    }
</style>