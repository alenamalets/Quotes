<template lang="pug">
        .container
            newquote(@quoteAdded="quotes.push($event)")
            allquotes(:quotes="quotes" @quoteDeleted="quotes.splice($event, 1)")
            .row 
                .col-sm-12.text-center
                    .alert.alert-info Info: click on a quote to delete it

</template>

<script>
    import AllQuotes from './components/AllQuotes.vue'
    import NewQuote from './components/NewQuote.vue'
    export default {
        data() {
            return {
                maxQuotes: 10,
                quotes: ['my first quote'],
            }
        },
        components: {
            allquotes: AllQuotes,
            newquote: NewQuote,
        }
    }
</script>

<style>
</style>
