<template> <!--The code for global navigation!-->
<v-container fluid class>
  <v-card>
     <v-toolbar
      color="purple"
      black = "false"
      flat
      right
      >
      <Nlogo/><br> <!--The logo on the left!-->
      <h3>Nanavati Hospital</h3> <!--the text 'Nanavati Hospital' after it!-->
      <v-spacer></v-spacer>
      <v-btn class='ma-2'depressed small light>Book appointment</v-btn> <!--Button for book an appointment!-->
      <v-btn class='ma-2'depressed small color="green">Quick Enquiry</v-btn> <!--Button for quick enquiry!-->
      <br>
      <v-divider vertical> </v-divider> 
      <h6> Patient portal</h6>
       <v-btn class="ma-2" x-small tile color="purple" purple>Login</v-btn> <!--Button for login!-->
       <v-btn class="ma-2" x-small color="green">Register</v-btn> <!--Button for register!-->
      
      
      <template v-slot:extension> <!--Code for the tabs below(2nd line)!-->
        <v-tabs
          v-model="tab"
          align-with-title
        >
          <v-tabs-slider color="white"></v-tabs-slider>

          <v-spacer></v-spacer>
          <v-tab show-arrows v-for="item in items" :key="item">
            {{ item }}
            <v-tab-item
        
          </v-tab> <!--The search text field code!-->
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
  </v-container>
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