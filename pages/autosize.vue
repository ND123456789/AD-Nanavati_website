<template>
  <v-container class="grey lighten-5">
    <v-row
      v-for="n in 11"
      :key="n"
      :class="n === 1 ? 'mb-6' : ''" 
      no-gutters
    >
    <!-- mb is for adding gutters. mb is bottom margin which is now set to 6!-->
    <!-- no-gutters prevents gutters. try deleting it!-->
      <v-col
        v-for="k in n + 2"
        :key="k"
      >
        <v-card
          class="pa-2"
          outlined
          tile
        >
          {{ k }} of {{ n + 1 }}
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>