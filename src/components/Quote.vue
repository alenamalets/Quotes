<template lang="pug">
    .col-sm-6.col-md-4.col-lg-3
        .panel.panel-default
            .panel-body.quote
                slot
</template>


<script>

</script>

<style>
    .panel-body {
        font-family: "Arizonia", cursive;
        font-size: 24px;
        color: #6e6e6e;
    }
    .quote {
        cursor: pointer;
    }

    .quote:hover {
        background-color: #ffe2e2;
    }
</style>