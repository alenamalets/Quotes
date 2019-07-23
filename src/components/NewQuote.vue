<template lang="pug">
    .row 
        form
            .col-sm-8.col-sm-offset-2.col-xs-12.col-md-6.col-md-offset-3.form-group
                label Quote
                textarea(class="form-control" rows="3" v-model="quote") 
            .col-sm-8.col-sm-offset-2.col-xs-12.col-md-6.col-md-offset-3.form-group
                button.btn.btn-primary(@click.prevent="createNew") Add quote 

</template>


<script>
export default {
  data() {
      return {
          quote: '',
      }
  },
  methods: {
      createNew() {
          
      }
  }
}
</script>

<style>

</style>