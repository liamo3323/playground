<template>
    <div>
        <main>
        
          <Header/>

        <h1>\\ Welcome to the App! // </h1>  
        <p><br><br><br>  This will link you to the page with more content n stuff!  </p> 
         <NuxtLink to="/contents">
            Link to CONTENT <br><br>
        </NuxtLink>
         <a href="http://localhost:3000/contents">content page via local host but not SPA</a>
    


        <div><br></div>
        
        <button @click="increment">Add 1</button>

        <p>Count is: {{ counter }}<br><br></p>


        <input v-model="message" placeholder="type here!">
        <p>Message is: {{ message }}</p>

        <h1> Movies: [Json file] </h1>

           <Footer/>

        </main>
    </div>
</template>

<!-- ||||||||||||||||||||||||||||||||||| -->

<script lang="ts">

import Vue from 'vue'
import Footer from '~/components/Footer.vue';
import Header from '~/components/Header.vue';

export default Vue.extend({
    name: "Homepage",
    data() {
        return {
            counter: 0,
            message: ""
        };
    },
    methods: {
        increment: function () {
            this.counter++;
        },
        message: function () {
            this.message;
        },
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
      color: rgb(209, 75, 126);
  }
</style>
