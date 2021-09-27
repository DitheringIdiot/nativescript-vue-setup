<template web>
  <div class="w-page">
    <div class="w-container">
      <img
        src="~/assets/logo.png"
        alt="logo"
      >
      <HelloWorld :msg="msg" />
    </div>
  </div>
</template>
<!-- -->
<template native>
  <Page>
    <ActionBar :title="navbarTitle" />
    <GridLayout rows="auto, auto">
      <!-- copy-webpack-plugin copies asset from src/assets to project output/build directory /assets -->
      <Image
        src="~/assets/logo.png"
        row="0"
        class="m-20"
      />
      <HelloWorld
        :msg="msg"
        row="1"
      />
    </GridLayout>
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
