<template> <!--The code for global navigation!-->
  <v-card>
      
     <v-toolbar
      color="purple"
      black="false"
      flat
      right
      extension
      >
      <v-row>
        <v-col
          cols="12"
          md="6"
          sm="4"
          xs="2"
          >
          <v-card
            flat
            color="purple"
            class="ml-3 mt-7 mt-xs-5"
            >
            <Nlogo/> <!--The logo on the left!-->
          </v-card>
          <h5
          class="d-none d-sm-block">Nanavati Hospital</h5> <!--the text 'Nanavati Hospital' after it!-->
        </v-col>
        <v-col
          cols="12"
          md="6"
          sm="8"
          xs="10"
          class="d-flex"
          >
          <v-btn  group class="mt-md-10 mt-sm-10 "depressed small light>Book appointment</v-btn> <!--Button for book an appointment!-->
          <v-btn class="mt-md-10 ml-3 mt-sm-10 ma-xs-auto" depressed small color="green">Quick Enquiry</v-btn>
          <div 
          class="d-none d-sm-block">
          <!--<caption>Patient portal</caption>!-->
          <v-btn 
          group
          class="mt-md-10 mt-sm-10 ml-3 ma-xs-auto" x-small outlined color="white">Login</v-btn>
          <v-btn class="mt-md-10 mt-sm-10 ma-xs-auto" x-small color="green">Register</v-btn> <!--Button for quick enquiry!-->

          </div>
          
        </v-col>
      </v-row>

        <!--<v-responsive
            v-if="n === 2"
            :key="`width-${n}`"
            width="100%"
          ></v-responsive>!-->
      
      <template 
        v-slot:extension> <!--Code for the tabs below(2nd line)!-->
        <v-tabs
          v-model="tab"
          align-with-title
          class="d-none d-sm-block"
          >
          <v-tabs-slider color="white"></v-tabs-slider>
          <v-spacer></v-spacer>
          
          <v-tab 
            class="mt-md-3 mt-sm-4" 
            show-arrows v-for="item in items" :key="item">
            {{ item }}
          </v-tab>

          <div class="d-md-none"> <!--The search text field code!-->
            <v-btn
              retain-focus-on-click
              icon color="white"
              depressed 
              class=" pa-0 mb-sm-6"
              >
              <v-icon>mdi-magnify</v-icon>
            </v-btn>
          </div>
          <div class="d-none d-md-block"> <!-- This command hides the search text field on small devices.The sodes works!-->
            <v-text-field
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