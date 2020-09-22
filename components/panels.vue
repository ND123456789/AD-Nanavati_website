<template>
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
               <h3> ICU rooms not available</h3>
                <!--<Autocomplete/>!-->
                <v-autocomplete
                  :items="['Borivali', 'Malad']"
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
                <v-expansion-panel-content>
                <v-btn large color="green">Call now</v-btn>
                +91 9890834091
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
        <v-col
          cols="12"
          md="4"
          sm="4"
          > <!--A separte column for instant doc and helplie number!-->
          <v-card
            class="mx-auto"
            max-width="280"
            light
            single
            raised
            >
            <v-list-item three-line> 
              <v-list-item-content> <!--Card for instant doctor!-->
                <v-list-item-title class="headline mb-1"><b>Instant Doctor</b></v-list-item-title>
                <v-list-item-subtitle>+91 937174902</v-list-item-subtitle>
              </v-list-item-content>
              <v-icon x-large color="green darken-1">mdi-phone</v-icon>
            </v-list-item>

            <v-card-actions>
              <v-btn large color="green">Call now</v-btn>
            </v-card-actions>
            </v-card>
            <br></br>
            <v-card 
              class="mx-auto"
              max-width="280"
              light
              single
              outlined
              >
              <v-list-item two-line>
                <v-list-item-content> <!--card for helpline!-->
                  <v-list-item-title class="headline mb-1"><h5>Helpline</h5></v-list-item-title>
                  <v-list-item-subtitle><h5>+91 937174902</h5></v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
              <v-card-actions>
              <v-btn text large color="green">Call now</v-btn>
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