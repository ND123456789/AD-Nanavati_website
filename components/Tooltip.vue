<template>
  <div>
    <div class="d-flex">
    </div>
    <v-container fluid class="pa-7">
      <v-row>
        <v-col
          cols="12"
          sm="4"
          md="8"
          >
          <v-expansion-panels
            v-model="panel"
            light
            focusable
            tile
            single
            >
            <v-expansion-panel>
              <v-expansion-panel-header><h2>ICU Beds</h2></v-expansion-panel-header>
              <v-expansion-panel-content>
                ICU rooms not available
                <Autocomplete/>
              </v-expansion-panel-content>
            </v-expansion-panel>
          </v-expansion-panels>
        </v-col>
        <v-col
        cols="12"
        md="4"
        sm="2"
        >
          <v-card
              class="mx-auto"
              max-width="344"
              light
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