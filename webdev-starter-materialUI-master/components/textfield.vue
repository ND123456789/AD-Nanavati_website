<template>
  <v-row align="center">
    <v-col cols="12">
      <v-select
        :items="items"
        :menu-props="{ top: true, offsetY: true }"
        label="Hospitals list"
      ></v-select>
      
    </v-col>
  </v-row>
</template>

<script>
  export default {
    data: () => ({
      items: 
       Borivali [
         {'Apex hospital', 'karuna hospital'},
       ],
       Malad [
         {'national hospital', 'AB' },
       ]
    }),
  }
</script>