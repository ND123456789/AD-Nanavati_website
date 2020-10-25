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
          href: 'breadcrumbs_dashboard',
        },
        {
          text: 'Emergency Service',
          disabled: false,
          href: 'breadcrumbs_link_1',
        },
        
      ],
    }),
  }
</script>