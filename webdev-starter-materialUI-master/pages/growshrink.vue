<template>
  <v-container class="grey lighten-5">
    <v-row
      class="mb-2"
      no-gutters
    >
      <v-col
        v-for="n in 3"
        :key="n"
        :cols="n ===3 ? 1 : 4"
      >
        <v-card
          class="pa-2"
          tile
          outlined
        >
          col
        </v-card>
      </v-col>
    </v-row>

    <v-row no-gutters>
      <v-col
        v-for="n in 2"
        :key="n"
        :cols="n === 1 ? 2 : 4"
      >
        <v-card
          class="pa-2"
          tile
          outlined
        >
          col-{{ n === 1 ? 8 : 4 }} <!--curly brackets are only used to display!-->
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>