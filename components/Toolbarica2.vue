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
          md="8"
          sm="4"
          >
          <v-card
          flat
          color="purple"
          class="ml-3 mt-7"
          >
          <Nlogo/> <!--The logo on the left!-->
          </v-card>
          <h5>Nanavati Hospital</h5> <!--the text 'Nanavati Hospital' after it!-->
        
        </v-col>
        <v-col
          cols="12"
          md="4"
          sm="8"
          >
          <v-btn class="mt-10 mr-sm-1"depressed small light>Book appointment</v-btn> <!--Button for book an appointment!-->
          <v-btn class="mt-10 ml-sm-1" depressed small color="green">Quick Enquiry</v-btn>
          <v-btn class="mt-10 ml-sm-1 ml-md-5" x-small color="purple">Login</v-btn>
          <v-btn class="mt-10 ml-sm-1" x-small color="green">Register</v-btn> <!--Button for quick enquiry!-->
        </v-col>
      </v-row>

        <v-responsive
            v-if="n === 2"
            :key="`width-${n}`"
            width="100%"
          ></v-responsive>
      
          <template 
            v-slot:extension> <!--Code for the tabs below(2nd line)!-->
            <v-tabs
              class="mt-md-3 mt-sm-6"
              v-model="tab"
              align-with-title
              >
              <v-tabs-slider color="white"></v-tabs-slider>

              <v-spacer></v-spacer>
              <v-tab 
              show-arrows v-for="item in items" :key="item">
                {{ item }}
                <v-tab-item
            
              </v-tab>  <!--The search text field code!-->
                <v-text-field
                  append-icon="mdi-magnify"
                  class="mx-sm-1"
                  flat
                  hide-details="auto"
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