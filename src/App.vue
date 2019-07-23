<template lang="pug">
        .container
            allquotes(:quotes="quotes")
</template>

<script>
    import AllQuotes from './components/AllQuotes.vue'

    export default {
        data() {
            return {
                maxQuotes: 10,
                quotes: ['my first quote'],
            }
        },
        components: {
            allquotes: AllQuotes,

        }
    }
</script>

<style>
</style>
