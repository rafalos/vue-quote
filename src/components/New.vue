<template lang="html">
<div>
<h4>Quote</h4>
<textarea v-model="userQuote" @keydown.enter.prevent="addQuote"></textarea>
<button class="btn btn-primary" @click="addQuote">Add quote</button>
</div>
</template>

<script>
export default {
  data: function(){
    return {
        userQuote: ""
    }
  },
  methods: {
    addQuote(){
      this.$emit("quoteAdded", this.userQuote)
      this.userQuote=""
    }
  }
}
</script>

<style lang="css" scoped>
div {
  width: 50%;
  margin: 10px auto;
}

textarea {
  width: 100%;
}
</style>
