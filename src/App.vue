<template>
  <v-app class="white lighten-4">
    <app-navbar></app-navbar>
    <v-content fluid fill-height>
      
        <router-view></router-view>

     
    </v-content>
     <app-footer></app-footer>
    
  </v-app>
</template>

<script>

import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';
export default {
  name: 'App',
  components:{
   'app-navbar' : Navbar,
   'app-footer' : Footer 
 },
  data () {
      return {
      
    }
  }
}
</script>
<style>
  html { 
    overflow-y: auto; 
  }
#app{
  font-family: 'KoHo', sans-serif;
}

</style>style>
