<!-- For the same task of location specific hospital,I tried using table. It wanted it to have 2 colummn.
one which has the lists of location and the other column which has the list of the hospitals to that
specific location. But it didnt work out since it showed an error.!-->
<template>
  <div>
    <v-simple-table
      :dense="dense"
      :fixed-header="fixedHeader"
      :height="height"
    >
      <template v-slot:default>
        <thead>
          <tr>
            <th class="text-left">Location</th>
            <th class="text-left">Hospital names</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="item in Mytask" :key="item.name">
            <td>{{ item.name }}</td>
            <td>{{ item.hospitals }}</td>
          </tr>
        </tbody>
      </template>
    </v-simple-table>

    <v-row>
      <v-col cols="12" md="6">
      <v-text-field
        
        class="mx-4"
        flat
        hide-details
        label="Type the location"

        solo-inverted
      ></v-text-field>
        <!--<v-text-field
          v-model="height"
          class="mx-4"
          label="Height - px"
          max="500"
          min="1"
          step="1"
          style="width: 125px"
          type="number"
          @keydown="false"
        ></v-text-field>!-->
      </v-col>
      
    </v-row>
  </div>
</template>

<script>
  export default {
    data: () => ({
      dense: false,
      fixedHeader: false,
      height: 300,
      Mytask: [
        {
          name: 'Borivali',
          hospitals: 'Apex hospitals', 'Karuna',
        },
        {
          name: 'Goregaon',
          hospitals: 'SRV hospitals', 'Sujay hospital',
        },
        {
          name: 'Malad',
          hospitals: 'Suvarna Hospitals', 'Malad society hospital',
        },
        {
          name: 'Andheri',
          hospitals: 'Seven hills Hospitals',
        },
        
      ],
    }),
  }
</script>