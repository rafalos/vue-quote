<template lang="html">
  <div>
  <h2>Quotes Added</h2>
  <div id="progressBar">
      <div id="progressLine" :style="{width: quotesNumber*10 + '%'}">
        <h3 class="text-center" >{{quotesNumber}}/10 </h3>
      </div>
  </div>
  </div>
</template>

<script>
export default {
  props: {
    "quotesNumber": Number
  }
}
</script>

<style lang="css" scoped>
  #progressBar {
    border: 1px solid black;
    margin: 5px 0 5px 0;
    border-radius: 5px;
  }
  #progressLine {
    background: #347AB9;
      transition: 0.5s;
  }

  h3{
    margin: 0;
    color: white;
  }
</style>
