<template> <!--The code for global navigation!-->
  <v-card>
      
     <v-toolbar
      color="white"
      flat
      right
      extension
      >
      <v-row
        align-content-xl
        >
        <v-col
          cols="12"
          md="6"
          sm="4"
          xs="2"
          >
          <v-card
            flat
            color="#711843"
            class="ml-3 mt-7 mt-xs-5"
            >
            <Nlogo/> <!--The logo on the left!-->
          </v-card>
          <h5
          class="d-none d-sm-block">Nanavati Hospital</h5> <!--The name 'Nanavati Hospital' is hidden on
          devices smaller than sm-which means it is hidden in xs devices precisely!-->
        </v-col>
        <v-col
          cols="12"
          md="6"
          sm="8"
          xs="5"
          class="d-flex"
          >
          <v-btn  group class="mt-md-10 mt-sm-10 "depressed small color="#711843" dark>Book appointment</v-btn> <!--Button for book an appointment!-->
          <v-btn class="mt-md-10 ml-3 mt-sm-10 ma-xs-auto" depressed small color="green">Quick Enquiry</v-btn>
          <div 
          class="d-none d-sm-block">
          <!--<caption>Patient portal</caption>!-->
          <v-btn 
          group
          class="mt-md-10 mt-sm-10 ml-3 ma-xs-auto" x-small color="#711843">Login</v-btn>
          <v-btn class="mt-md-10 mt-sm-10 ma-xs-auto" x-small color="green">Register</v-btn> <!--Button for quick enquiry!-->

          </div>
          
        </v-col>
      </v-row>
      

      <!--Code for the tabs below(2nd line)!-->
      <!--Here, in md the search text field is visible. But in sm only a search/magnify button is available.
      In xs, the tabs are hidden, whereas the two buttons namely 'book an appointment' and 'quick enquiry' 
      are only visible with the Nanavati logo !-->
      <template 
        v-slot:extension> 
        <v-tabs
        right
        >
          <v-tab>patient Portal</v-tab>
          <v-tab>Intentioanl Patients</v-tab>
          <v-tab>Item Three</v-tab>
        </v-tabs>
          <!-- 'd-none d-sm-block' to hide tabs in devices smaller than sm!-->
          <v-tabs-slider color="#711843"></v-tabs-slider>
          <v-spacer></v-spacer>
          

          <!--The code for the search/magnify button which is only visible on md devices
           d-md-none is the display function which makes the search icon button visible only on md devices!-->
          <div class="d-md-none"> 
            <v-btn
              dark
              retain-focus-on-click
              icon color="#711843"
              depressed 
              class=" pa-0 mb-sm-6"
              >
              <v-icon>mdi-magnify</v-icon>
            </v-btn>

            <!--The search text field code!-->
          </div>
          <div class="d-none d-md-block"> <!-- This command hides the search text field on small devices!-->
            <v-text-field
              color="#711843"
              append-icon="mdi-magnify"
              class="mx-sm-1"
              flat
              hide-details="auto"
              label="Search"
              solo-inverted
            ></v-text-field>
          </div>
        </v-tabs>
      </template>
    
    </v-toolbar>
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