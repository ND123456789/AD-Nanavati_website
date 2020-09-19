<template>
  <div>
    <div class="d-flex">
    </div>
    <v-container fluid class="pa-3">
      <v-row>
        <v-col
          cols="12"
          sm="3"
          md="8"
          >
          <v-expansion-panels
            v-model="panel"
            light
            focusable
            tile
            single
            gutters
            >

            <v-expansion-panel>
              <v-expansion-panel-header><h2>ICU Beds</h2></v-expansion-panel-header>
              <v-expansion-panel-content>
               <h4> ICU rooms not available</h4>
                <Autocomplete/>
              </v-expansion-panel-content>
            </v-expansion-panel>

            <v-spacer></v-spacer>

            <v-expansion-panel>
                <v-expansion-panel-header><h2>Ambulance</h2></v-expansion-panel-header>
                <v-expansion-panel-content>
                <v-btn large color="green">Call now</v-btn>
                </v-expansion-panel-content>
              </v-expansion-panel>

              <v-spacer></v-spacer>

            <v-expansion-panel>
              <v-expansion-panel-header><h2>Do this in emergency</h2></v-expansion-panel-header>
              <v-expansion-panel-content>
               <Autocomplete2/>
              </v-expansion-panel-content>
            </v-expansion-panel>

          </v-expansion-panels>
        </v-col>
        <v-col
        cols="12"
        md="4"
        sm="1"
        >
          <v-card
              class="mx-auto"
              max-width="344"
              light
              single
              outlined
              >
              <v-list-item three-line>
                <v-list-item-content>
                  <v-list-item-title class="headline mb-1">Instant Doctor</v-list-item-title>
                  <v-list-item-subtitle>+91 937174902</v-list-item-subtitle>
                </v-list-item-content>

                  <v-icon x-large color="purple darken-2">mdi-dialpad</v-icon>
               </v-list-item>

                <v-card-actions>
                  <v-btn large color="green">Call now</v-btn>
                </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
      
      <!--<v-container fluid class="pa-7">
      <v-row>
        <v-col
            cols="12"
            md="8"
            sm="4"
            > 
              <v-expansion-panels
                  v-model="panel"
                  light
                  focusable
                  tile
                  multiple
                  
                  >        
                <v-expansion-panel>
                  <v-expansion-panel-header><h2>Do this in emergency</h2></v-expansion-panel-header>
                  <v-expansion-panel-content>
                    <Autocomplete2/>
                  </v-expansion-panel-content>
                </v-expansion-panel>
              </v-expansion-panels>
          </v-col>
      </v-row>!-->
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