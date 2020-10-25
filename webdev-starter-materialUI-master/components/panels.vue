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
              <v-expansion-panel-header elevation="2"><h2>ICU Beds</h2></v-expansion-panel-header>
              <v-expansion-panel-content>
               <h3 class="mt-5"> ICU rooms not available</h3>

                <!-- Selectlocation enables users to select a specific location. Whereas, selecthospital enables users
                to selct a hospital from a list of hospitals belonging to a specific hospital!-->                
                <Selectlocation/>
                <Selecthospital/>
                
              </v-expansion-panel-content>
            </v-expansion-panel>
        
            <v-expansion-panel
              hover
              focusable> <!--panel for Nanavati ambulance!-->
              <v-expansion-panel-header><h2>Nanavati Ambulance Number</h2></v-expansion-panel-header>
              <v-expansion-panel-content >
              <v-btn elevation="5" class="mt-3 mr-3" large color="green" dark> Call Now </v-btn>
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
            rounded
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
              <v-btn elevation="3" class="white--text" large color="#711843">Call now</v-btn>
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