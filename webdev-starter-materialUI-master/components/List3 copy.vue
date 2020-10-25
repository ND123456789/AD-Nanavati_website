<template>
  <v-container fluid>
    <v-row align="center">
      <v-col class="d-flex" cols="12" sm="6">
        <v-select
          :items="Borivali"
          label="Click to know all the hospitals in this location"
        ></v-select>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    data: () => ({
      Borivali: [
        {
          Location: "Borivali", 
          Hospital: "Apex hospital",
        }
          ],
    }),
  }
</script>