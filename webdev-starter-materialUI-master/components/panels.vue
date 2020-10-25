<template>
<!-- The panels were originally meant to be buttons that behave like 
tabs(in the XD deign). But afetr searching a lot, I realized I need to 
use either tabs or buttons for this. I couldnt find medical icons in the
veutify icon library.!--> 
  <div>
    <div class="d-flex">
    </div>
    <v-container fluid class="pa-3"> <!--padding pa!-->
      <v-row>
        <v-col
          cols="12"
          sm="8"
          md="8"
          >
          <v-expansion-panels
            v-model="panel"
            light
            focusable
            tile
            single
            >

            <v-expansion-panel> <!--panel for ICU beds!-->
              <v-expansion-panel-header><h2>ICU Beds</h2></v-expansion-panel-header>
              <v-expansion-panel-content>
               <h3 class="mt-5"> ICU rooms not available</h3>

               <!-- What i wanted is, when user enters Borivali in first text field, the second text field should show 
               the corresponding hospitals in Borivali. But is user enters Malad instead of Borivali, the second text field
               should show the corresponding hospitals in Malad instead of Borivali.!-->

               <!--Here in this autocomplete i wanted to have to text fields wherein, the first asks about the 
               location and the other one displays the corresponding hospitals for that location. I could only 
               get that for Borivali. I couldn't trigger the 2nd text field based on the inputs of 2st text field!--> 

               <!-- So I tried the code below. I made 2 different autocompletes. First one which holds the names of all 
               the locations. And the second one which hold the names of all the corresponding hospitals in that specific location.
               When user types Borivali, 'items' in (location) 1st autocomplete should trigger 'items' in 2nd autocomplete
               (all the hospital names). Similarly, When Malad is typed, instant from autocomplete 1 should trigger 
               instant in autocomplete 2. But this didn't work because the autocomplete only recognized items but not instant.
               i even tried this with text fields, lists, tables but couldn,t crack it!-->

                <v-autocomplete
                  :items="['Borivali']" 
                  :instant="['malad']"
                  label="Enter your location"
                  flat
                  light
                  clearable
                  hide-no-data
                  hide-details
                  single
                ></v-autocomplete>
                <v-autocomplete
                  :items="['Apex Multi-Speciality Hospitals', 'Karuna Hospital', 'National Hospitals']"
                  :instant="['Malad community hospital', 'Thunga hospital']"
                  label="Hospitals list"
                  single
                  ></v-autocomplete>
                
              </v-expansion-panel-content>
            </v-expansion-panel>
        
            <v-expansion-panel> <!--panel for Nanavati ambulance!-->
                <v-expansion-panel-header><h2>Nanavati Ambulance Number</h2></v-expansion-panel-header>
                <v-expansion-panel-content >
                <v-btn depressed class="mt-3 mr-3" large color="green" dark> Call Now </v-btn>
                </v-expansion-panel-content>
              </v-expansion-panel>

            <v-expansion-panel> <!--panel for do this in emeergency!-->
              <v-expansion-panel-header><h2>Do this in emergency</h2></v-expansion-panel-header>
              <v-expansion-panel-content>
              <br> </br>
               <!--<Autocomplete2/>!-->
               <dothis/> <!--the tabs component!-->
              </v-expansion-panel-content>
            </v-expansion-panel>

          </v-expansion-panels>
        </v-col>

        <!--The cards 'instant doctor' and 'helpline number' were made responsive because although 
        they are secondary tasks, they are critical part of this page . They needed to be placed such
        that they dont disturb the primary function of this page. Hence, in md and sm devices they are placed 
        besides the panels, but in xs devices they are placed after the panels.!-->

        <v-col
          cols="12"
          md="4"
          sm="4"
          >  <!--A separte column for instant doc and helpline number!-->
          <v-card
            class="mx-auto"
            max-width="280"
            color="#711843"
            light
            single
            outlined
            raised
            >
            <v-list-item three-line> 
              <v-list-item-content
              > <!--Card for instant doctor!-->
                <v-list-item-title
                 class="headline mb-1" ><b class="white--text">Instant Doctor</b></v-list-item-title>
                <v-list-item-subtitle class="white--text">+91 937174902</v-list-item-subtitle>
              </v-list-item-content>
              <v-icon x-large color="white">mdi-phone</v-icon>
            </v-list-item>

            <v-card-actions>
              <v-btn large color="white">Call now</v-btn>
            </v-card-actions>
            </v-card>
            <br></br>
            <v-card 
              class="mx-auto"
              max-width="280"
              light
              single
              outlined
              raised
              >
              <v-list-item two-line>
                <v-list-item-content> <!--card for helpline!-->
                  <v-list-item-title class="headline mb-1"><h5>Helpline</h5></v-list-item-title>
                  <v-list-item-subtitle><h5>+91 937174902</h5></v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
              <v-card-actions>
              <v-btn text large color="#711843">Call now</v-btn>
              </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
  export default {
    data: () => ({
      panel: [0, 1],
      disabled: false,
      readonly: false,
    }),
  }
</script>