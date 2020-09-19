<template>
  <v-card>
    <v-toolbar
      color="purple"
      black = "false"
      flat
      >
          
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-row>
        <v-col
            <v-col
              cols="9"
              sm="8"
            >
            
            Nanavati

        </v-col>
      </v-row>

      <v-spacer></v-spacer>

      <v-tab>Book an Appointment</v-tab>
     
      <v-tab>Quick enquiry</v-tab>

       <v-divider vertical></v-divider>
       <h6>Patient Portal</h6>
       <v-btn class="ma-2" tile color="purple" purple>Login</v-btn>
       <v-btn class="ma-2" outlined color="white">Outlined Button</v-btn>
      
      <template v-slot:extension>
        <v-tabs
          v-model="tab"
          align-with-title
        >
          <v-tabs-slider color="white"></v-tabs-slider>

          <v-spacer></v-spacer>
          <v-tab v-for="item in items" :key="item">
            {{ item }}
            <v-tab-item
        
          </v-tab>
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