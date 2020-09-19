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
          'Borivali east',
          'Borivali west',
          'Malad',
          'Dahisar',
          'Kandivali',
          'Goregaon',
          'Jogeshwari',
          
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