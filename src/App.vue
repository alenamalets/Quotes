<template lang="pug">
        .container
            newquote(@quoteAdded="quotes.push($event)")
            allquotes(:quotes="quotes")
            
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
