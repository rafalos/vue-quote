<template lang="html">
<div class="row" id="quoteContainer">
  <app-quotes v-for="(quote, index) in quotes" @click.native="removeQuote(index)">
    <h1>{{quote}}</h1>
  </app-quotes>
</div>
</template>

<script>
import Quote from "./Quote.vue"
export default {
  props: {
    quotes: Array
  },
  components: {
    appQuotes: Quote
  },
  methods: {
    removeQuote(index) {
      this.$emit("quoteRemoved", index)
      console.log(index)
    }
  }
}
</script>

<style lang="css">
#quoteContainer {
  margin: 3px;
}

.quoteBox {
  border: 1px solid black;
}
</style>
