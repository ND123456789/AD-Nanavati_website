<template>
<!-- How do I link selectlocation's data with select hospital's data. When I chose borivali in selectlocation,
the lists hospitals linked to borivali should be showed up in selecthospital. But when I select Malad, the list of hospitals linked 
to malad shouls be showed up.!--> 
  <v-select
    :items="Borivali"
    :item="Malad"
     label="Choose the hospital"
     raised
     light
     clearable
     hide-no-data
     hide-details
     single
     >
  </v-select>
</template>    
  <script>
    export default {
      data: () => ({
        Borivali: ['Lotus Multi-Speciality Hospital', 'National Hospitals', 'Apex Multi-speciality Hospital' ],
        Malad: ['Malad Hospital', 'Suvarna Hospital' ],
      }),
    }
  </script>