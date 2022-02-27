<template>
    <div>
    <Header/>
      <p>\\ ThIs iS  tHe pAgE wItH cOntEnt //</p>
      <NuxtLink to="/">
            Link to INDEX <br><br>
        </NuxtLink>
    <Footer/>
    </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Footer from '~/components/Footer.vue';
import Header from '~/components/Header.vue';

export default Vue.extend({
  name: 'Content',

  components: { Header, Footer }
})
</script>




<!-- Adding styling  to a specific page helps with organizing, adding it to the config will change the global styling -->
<style lang="scss">
  body {
      padding: 2.5%;
      text-align: center;
      font: 150% Helvetica, sans-serif;
      color: red;
  }
</style>
