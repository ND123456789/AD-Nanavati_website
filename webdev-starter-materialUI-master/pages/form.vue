<template>
  <v-row justify="center">
    <v-dialog v-model="dialog" persistent max-width="1000px">
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          color="primary"
          dark
          v-bind="attrs"
          v-on="on"
        >
          Open Dialog
        </v-btn>
      </template>
      <v-card>
        <v-card-title>
          <span class="headline">User Profile</span>
        </v-card-title>
        <v-card-text>
          <v-container>
            <v-row>
            <v-spacer></v-spacer>
            <v-btn color="blue darken-1" text @click="dialog = false">save and exit</v-btn>
                      
                <v-col cols="12" sm="12" md="4">
                <v-text-field label="Legal first name*" required></v-text-field>
              </v-col>
              <v-col cols="12" sm="6" md="4">
                <v-text-field label="Legal middle name" hint="example of helper text only on focus"></v-text-field>
              </v-col>
              <v-col cols="12" sm="5" md="4">
                <v-text-field
                  label="Legal last name*"
                  hint="example of persistent helper text"
                  persistent-hint
                  required
                ></v-text-field>
              </v-col>
              <v-col cols="5">
                <v-text-field label="Email*" required></v-text-field>
              </v-col>
              <v-col cols="6">
                <v-text-field label="Password*" type="password" required></v-text-field>
              </v-col>
              <v-col cols="12" sm="6">
                <v-select
                  :items="['0-17', '18-29', '30-54', '54+']"
                  label="Age*"
                   required
                ></v-select>
              </v-col>
              <v-col cols="12" sm="6">
               <v-autocomplete
                  :items="['Anoushka Shankar-Lasya', 'Aman Manch', 'Soccer', 'Garaj GAraj Jugalbandi', 'poppish classical', 'Sarod', 'Classical vocal', 'Coding']"
                  label="fav music"
                  single
                ></v-autocomplete>
               </v-col>
               <v-col cols="12" sm="12">
                <v-autocomplete
                  :items="['Skiing', 'Ice hockey', 'Soccer', 'Basketball', 'Hockey', 'Reading', 'Writing', 'Coding', 'Basejump']"
                  label="Interests"
                  multiple
                ></v-autocomplete>
              </v-col>
            </v-row>
          </v-container>
          <small>*indicates required field</small>
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="red" text @click="dialog = true">Close</v-btn>
          <v-btn color="green" text @click="dialog = false">Save</v-btn>
          <v-btn color="red" text @click="dialog = false">Later</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-row>
</template>

<script>
  export default {
    data: () => ({
      dialog: false,
    }),
  }
</script>