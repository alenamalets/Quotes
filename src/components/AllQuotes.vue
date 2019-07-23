<template lang="pug">
    .row 
        quote(v-for='quote in quotes') {{quote}} 
</template>


<script>
import Quote from './Quote.vue'
export default {
    props: ['quotes'],
    components: {
        quote: Quote,
    }
}
</script>

<style>

</style>
