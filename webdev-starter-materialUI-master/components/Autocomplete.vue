<template>
        <v-autocomplete
          v-model="select"
          :items="items"
          :search-input.sync="search"
          cache-items
          class="mx-4"
          flat
          light
          clearable
          hide-no-data
          hide-details
          label="Enter your location to find nearest hospital"
          solo-inverted
        ></v-autocomplete>
</template>
          

<script>
  export default {
    data () {
      return {
        loading: false,
        items: [],
        search: null,
        select: null,
        states: [
          'Borivali east- Apex Multi-speciality hospitals',
          'Borivali east- Lotus Multi-speciality hospitals',
          'Borivali west- Karuna Hospital',
          'Malad- Surana hospital and research center',
          'Malad- Thunga hospital',
          'Dahisar- Pinnacle hospital',
          'Dahisar- Pragati Multi-speciality hospital',
          'Goregaon- Kapadia Multispeciality Hospital',
          'Goregaon- Vishwa Kripa Hospital',
          'Andheri- Critical Care Hospital',
          'Andheri- Mukund Hospital',
          
        ],
      }
    },
    watch: {
      search (val) {
        val && val !== this.select && this.querySelections(val)
      },
    },
    methods: {
      querySelections (v) {
        this.loading = true
        // Simulated ajax query
        setTimeout(() => {
          this.items = this.states.filter(e => {
            return (e || '').toLowerCase().indexOf((v || '').toLowerCase()) > -1
          })
          this.loading = false
        }, 500)
      },
    },
  }
</script>