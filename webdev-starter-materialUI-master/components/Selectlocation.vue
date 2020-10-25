<template>
  <v-select
    :items="items"
     label="Enter your location"
     flat
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
        items: ['Borivali', 'Malad', 'Andheri', 'Goregaon' , 'Bandra'],
      }),
    }
  </script>