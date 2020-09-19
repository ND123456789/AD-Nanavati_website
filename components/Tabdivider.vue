<template>


  <v-app-bar
    color="purple"
    dark fixed app

  > <v-app-bar-nav-icon></v-app-bar-nav-icon>
    <v-toolbar-title>Nanavati</v-toolbar-title>

    <v-divider
      class="mx-4"
      vertical
    ></v-divider>

    <v-spacer></v-spacer>

   
      <v-btn text>
        Patient Portal
      </v-btn>

      <v-divider vertical></v-divider>

      <v-btn text>
        Doctors
      </v-btn>

      <v-divider vertical></v-divider>

      <v-btn text>
        International Patients
      </v-btn>

      <v-divider vertical></v-divider>

      <v-btn text>
        Outstation OPD
      </v-btn>

      <v-divider vertical></v-divider>

       <v-text-field
        append-icon="mdi-magnify"
        class="mx-4"
        flat
        hide-details
        label="Search"
        solo-inverted
      ></v-text-field>

  
           
          </v-list-item>
        </v-list>
      
    </v-toolbar-items>

    
  </v-app-bar>
 
</template>