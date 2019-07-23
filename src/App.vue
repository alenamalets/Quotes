<template lang="pug">
        .container
            myheader(:maxQuotes="maxQuotes" :quoteCount="quotes.length")
            newquote(@quoteAdded="newQuote")
            allquotes(:quotes="quotes" @quoteDeleted="quotes.splice($event, 1)")
            .row 
                .col-sm-12.text-center
                    .alert.alert-info Info: click on a quote to delete it

</template>

<script>
    import Header from './components/Header.vue'
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
            myheader: Header
        },
        methods: {
            newQuote(quote) {
                if(this.quotes.length >= this.maxQuotes) {
                    return alert('Please delete quotes first')
                }
                this.quotes.push(quote);
            }
        }
    }
</script>

<style>
</style>
