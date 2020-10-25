<template>
<!--Here, I tried to link the locations and hospitals. Through this code
what I wanted was that when the users enter borivali, then "Apex hospitals" and "Karuna Hospital" 
should be displayed. And when users enter malad, then "National hospital" and "Malad hospital" should be displayed.
I wrote the scrit accordingly but it should an error. 
The error said this - 
Object._raise (E:\Assignments\SEM 3\TI coding\WEbsite coding\AD-Nanavati_Website\AD-Nanavati_website\AD-Nanavati_website\webdev-starter-materialUI-master\node_modules\@babel\parser\lib\index.js:799:17)
at Object.raiseWithData (E:\Assignments\SEM 3\TI coding\WEbsite coding\AD-Nanavati_Website\AD-Nanavati_website\AD-Nanavati_website\webdev-starter-materialUI-master\node_modules\@babel\parser\lib\index.js:792:17)!-->
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
         items: 
      
          borivali: [
          "Apex hospitals",
          "Karuna Hospital",
        ],
    
         {
           Malad: [
          "National hospital",
          "Malad hospital",
         ],
         }

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