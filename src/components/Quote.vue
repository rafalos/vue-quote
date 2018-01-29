<template lang="html">
  <div class="col-lg-3 quoteBox">
    <slot>
    </slot>
  </div>
</template>

<script>
export default {
  }
</script>

<style lang="css" scoped>
div{
  text-align: center;
  font-family: "Arizonia";
  font-size: 50px;
  border-radius: 10px;
}
div:hover{
  background: #FFE1E4;
  cursor: pointer;

}

</style>
