<template>
    <div>

        <p>\\ ThIs iS  tHe pAgE wItH cOntEnt //</p>
      
        <NuxtLink to="/">
              Link to INDEX <br> <br>
          </NuxtLink>

            <li v-for="user in users" :key="user.id">         
              My name is: {{user.name}} and I am {{user.age}} years old! 
            </li> <br>

            <Card/>

    </div>
</template>



<script lang="ts">
import Vue from 'vue'

import Footer from '~/components/Footer.vue';
import Header from '~/components/Header.vue';
import usersData from '~/assests/users.json';


export default Vue.extend({
  name: 'Content',

  data(){
    return {
      users: usersData
    }
  },

  components: { Header, Footer }
})
</script>




<!-- Adding styling  to a specific page helps with organizing, adding it to the config will change the global styling -->
<style lang="scss">
  body {
      padding: 2.5%;
      text-align: center;
      font: 150% Helvetica, sans-serif;
      color: green;
  }
</style>
