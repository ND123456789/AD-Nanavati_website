<template>
  <v-card>
  
     <v-toolbar
      color="purple"
      black = "false"
      flat
      right
      >
      <Nlogo/><br>
      <h3>Nanavati Hospital</h3>
      <v-spacer></v-spacer>
      <v-btn class='ma-2'depressed small light>Book appointment</v-btn>
     
      <v-btn class='ma-2'depressed small light>Quick Enquiry</v-btn>
    <br>
      <v-divider vertical> </v-divider>
      <h6> Pateint portal</h6>
       <v-btn class="ma-2" x-small tile color="purple" purple>Login</v-btn>
       <v-btn class="ma-2" x-small outlined color="white">Register</v-btn>
      
      
      <template v-slot:extension>
        <v-tabs
          v-model="tab"
          align-with-title
        >
          <v-tabs-slider color="white"></v-tabs-slider>

          <v-spacer></v-spacer>
          <v-tab show-arrows v-for="item in items" :key="item">
            {{ item }}
            <v-tab-item
        
          </v-tab>
            <v-text-field
              append-icon="mdi-magnify"
              class="mx-4"
              flat
              hide-details
              label="Search"
              solo-inverted
            ></v-text-field>
          </v-tabs>
      </template>
    </v-toolbar>
    </v-tab-item>
    </v-tabs-items>
  </v-card>
</template>

<script>
  export default {
    data () {
      return {
        tab: null,
        items: [
          'Patient Portal', 'Doctors', 'International Patients', 'Outstation OPD',
        ],
        
      }
    },
  }
</script>