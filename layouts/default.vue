<template>
  <!--Your App Starts Here -->
  <v-app id="inspire">
    
    <!--Header -->
     
    <v-app-bar color="purple" dark fixed app>
          <v-toolbar-title>Nanavati</v-toolbar-title>
       <!-- Component Example -->
             <NanavatiLogo/> 
             <Tab/>
    
         </v-app-bar>

    <!-- Body -->
    <v-content light>
          <nuxt /> 
      
    </v-content>
    
    <!-- Footer -->
    <v-footer color="indigo" app>
      <span class="white--text">&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>

  </v-app>
</template>

<script>
export default {}
</script>

<style> 
  .white--text {
    border: 1px solid;
  }

   #inspire {
    background-color: white;
    colour: black;
  }
</style>