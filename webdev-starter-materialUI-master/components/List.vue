<template>
  
    <v-card
      class="mx-auto"
      max-width="400"
      light
      tile

    >
      
        <v-list-item-group v-model="item" color="primary">
          <v-list-item
            v-for="(item, i) in items"
            :key="i"

          >
            <v-list-item-hospital v-if="hospitalr">
              <v-img :src="item.hospital"></v-img>
            </v-list-item-hospital>
            <v-list-item-content>
              <v-list-item-title v-html="item.title"></v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-card>
  </v-row>
</template>

<script>
  export default {
    data: () => ({
      items: [
        {
          hospital: 'https://cdn.vuetifyjs.com/images/lists/1.jpg',
          title: 'Apex Multi-speciality hospitals',
        },
        {
          hospital: 'https://cdn.vuetifyjs.com/images/lists/2.jpg',
          title: 'Karuna hospital',
        },
        {
          hospital: 'https://cdn.vuetifyjs.com/images/lists/3.jpg',
          title: 'National hospital',
          
        },
        
      ],

      
      dense: false,
      twoLine: false,
      threeLine: false,
      shaped: true,
      flat: false,
      subGroup: true,
      nav: true,
      avatar:true,
      rounded: false,
    }),
  }
</script>