<template>
  <div>
    <div class="message">{{msg}}</div>
    <img
      src="~/components/icon.png"
      alt="logo"
    >
  </div>
</template>

<script lang="ts">
  import Vue from 'vue'
  export default Vue.extend({
    name: 'HelloWorld',
    props: {
      msg: {
        type: String,
        default: ''
      }
    }
  })
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.message {
  color: red;
}
</style>