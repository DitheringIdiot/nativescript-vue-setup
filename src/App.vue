<template web>
  <div class="w-page">
    <div class="w-container">
      <img
        src="~/assets/logo.png"
        alt="logo"
        height="20%"
        width="20%"
      >
      <HelloWorld :msg="msg" />
    </div>
  </div>
</template>

<template native>
  <Page>
    <StackLayout backgroundColor="#000">
      <TextView text="Multi\nLine\nText" />
    </StackLayout>
  </Page>
</template>

<script lang="ts">
  import Vue from 'vue'
  import HelloWorld from 'components/HelloWorld.vue';

  export default Vue.extend({
    name: 'home',
    components: {
      HelloWorld
    },
    data() {

      const { VUE_APP_MODE, VUE_APP_PLATFORM } = process.env;
      const msg = `Mode=${VUE_APP_MODE} and Platform=${VUE_APP_PLATFORM}`

      return {
        navbarTitle: 'Home.vue',
        msg
      }
    }
  })
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
