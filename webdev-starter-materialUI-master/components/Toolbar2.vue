<template>
  <v-toolbar extended light height="110 px"> 
      <v-row>
        <v-col
        cols="12"
        md="6"
        sm="4"
        xs="3"
        align="left"
        >
          <div
            class="mt-xs-auto">
            <Nlogo/>
          </div>
        </v-col>

        <v-col
        cols="12"
        md="6"
        sm="8"
        xs="6"
        align="right"
        class="d-flex"
        >
            
          <v-btn group class="mt-md-10 mt-sm-8 ma-xs-1 ma-md-1 ma-sm-1" depressed small color="#711843" dark>Book appointment<v-icon> mdi-chevron-right</v-icon></v-btn> <!--Button for book an appointment!-->
          <v-btn class="mt-md-10 mt-sm-8 ma-xs-1 ma-md-1 ma-sm-1 mr-md-2" depressed small color="green" dark>Quick Enquiry <v-icon> mdi-chevron-right</v-icon></v-btn>

          <div 
            class="d-none d-sm-block">
            <v-btn 
            group
            class="mt-md-10 mt-sm-8 ma-xs-auto" x-small color="#711843" dark>Login</v-btn>
            <v-btn class="mt-md-10 mt-sm-8 ma-xs-auto" x-small color="green" dark>Register</v-btn> <!--Button for quick enquiry!-->
          </div>
        </v-col>    
      </v-row>
      <template 
      v-slot:extension> 
        <v-tabs
          v-model="tab"
          background-color="transparent"
          align-with-title
          color="#711843"
          class="d-none d-sm-block"

          >
          <!-- 'd-none d-sm-block' to hide tabs in devices smaller than sm!-->
          <v-tabs-slider color="#711843"></v-tabs-slider>
          <v-spacer></v-spacer>
          
          <v-tab 
            show-arrows v-for="item in items" :key="item">
            {{ item }}
          </v-tab>

          <!--The code for the search/magnify button which is only visible on md devices
           d-md-none is the display function which makes the search icon button visible only on md devices!-->
          <div class="d-md-none"> 
            <v-btn
              retain-focus-on-click
              icon color="#711843"
              depressed 
              class=" pa-0 mb-sm-6">
              <v-icon>mdi-magnify</v-icon>
            </v-btn>

            <!--The search text field code!-->
          </div>
          <div class="d-none d-md-block"> <!-- This command hides the search text field on small devices!-->
            <v-text-field
              color="white"
              append-icon="mdi-magnify"
              class="mx-sm-1"
              hide-details="auto"
              label="Search"
              dense
              solo-inverted
            ></v-text-field>
          </div>
        </v-tabs>
      </template>
  </v-toolbar>
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