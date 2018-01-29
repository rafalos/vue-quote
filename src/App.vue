<template>
    <div class="container">
      <app-bar :quotesNumber="quotes.length"></app-bar>
      <app-new @quoteAdded="addQuote"></app-new>
      <appList @quoteRemoved="removeQuote" :quotes="quotes"></appList>
      <app-footer></app-footer>
    </div>
</template>

<script>
import ProgressBar from "./components/ProgressBar.vue"
import New from "./components/New.vue"
import List from "./components/List.vue"
import Footer from "./components/Footer.vue"
    export default {
      data: function(){
        return {
          quotes: []
        }
      },
      components:{
        appBar: ProgressBar,
        appNew: New,
        appList: List,
        appFooter: Footer
      },
      methods: {
        removeQuote(i) {
                this.quotes.splice(i, 1)
        },
        addQuote(quote){
          if(this.quotes.length>=10){
            return alert("Limit exceeded")
          }
            this.quotes.push(quote)
        }
      }
    }
</script>

<style>
</style>
