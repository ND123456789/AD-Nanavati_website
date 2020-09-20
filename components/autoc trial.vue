<template>
        <v-autocomplete
          v-model="select"
          :items="borivali" 
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
        select: null,
        search: null,
        // items: 
      
          borivali: [
          "Apex hospitals",
          "Karuna Hospital",
        ],
    
        // {
        //   Malad: [
        //   "National hospital",
        //   "Malad hospital",
        // ],
        // }

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