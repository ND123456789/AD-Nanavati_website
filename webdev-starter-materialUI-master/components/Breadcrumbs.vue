<template>
  <div>

    <v-breadcrumbs :items="items">
      <template v-slot:divider>
        <v-icon medium dark color="grey">mdi-chevron-right</v-icon>
      </template>
    </v-breadcrumbs>
  </div>
</template>

<script>
  export default {
    data: () => ({
      items: [
        {
          text: 'Home',
          disabled: false,
          href: 'http://localhost:3000/AD-Nanavati_website/',
        },
        {
          text: 'Emergency Service',
          disabled: false,
          href: 'http://localhost:3000/AD-Nanavati_website/Zmergency',
        },
        
      ],
    }),
  }
</script>