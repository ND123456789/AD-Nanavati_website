<template>
  <!--Your App Starts Here -->
  <v-app id="banner">
    
    <!--Header -->
     
    <!--<v-app-bar color="purple" dark fixed app>
          <v-toolbar-title>Nanavati</v-toolbar-title>
       <!-- Component Example -->
                  <Nlogo/>
                  <Toolbar/>
                  
                  
               
         

    <!-- Body -->
    <v-content light>
          <nuxt /> 
          
    </v-content>
    
    <!-- Footer -->
    <v-footer color="indigo" app>
      <span class="black--text">&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>

  </v-app>
</template>

<script>
export default {}
</script>

<style> 
  .black--text {
    border: 1px solid;
  }

   #banner {
    background-color: white;
    colour: black;
  }
</style>