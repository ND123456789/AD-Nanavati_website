<template>
  <v-toolbar extended light height="110 px"> 
  <!-- the height needed to be fixed, since in XS screen size,
  the logo was getting cut. This size perfectly baances!--> 

  <!-- The upper part of the toolbar is a row and the tabs are 
  placed in the next row. The logo is in a column and the buttons
  are placed in the nest column!-->
      <v-row> 
        <v-col
        cols="12"
        md="6"
        sm="4"
        xs="3"
        align="left"
        >
        <!-- The md, sm, xs sizes perfectly balance the responsive 
        behaviour on all the screens. Dont alter them, otherwise all 
        the sizes would have to be fixed for making it perfectly 
        responsive again!-->
          <div
            class="mt-xs-auto">
            <Nlogo/>
          </div>
        </v-col>

        <v-col
        cols="12"
        md="6"
        sm="8"
        xs="6"
        align="right"
        class="d-flex"
        >
        <!-- the buttons needed to be placed at a distance from the top,
        hence mt and sm screens is md screen is 10 for all the four buttons.
        In xs screen, the buttons came in the next row, so needed little margin 
        from all the sides, hence ma in xs screen is 1. In sm screens, balancing
        margin from all sides made it look balanced and properly placed. 
        The colour in the button makes the button coloured and writting dark/light
        makes the text in it be white/black. I wanted white text, so dark seemed right.!--> 
            
          <v-btn group elevation="5" class="mt-md-10 mt-sm-8 ma-xs-1 ma-md-1 ma-sm-1" depressed small color="#711843" dark>Book appointment<v-icon> mdi-chevron-right</v-icon></v-btn> <!--Button for book an appointment!-->
          <v-btn elevation="5" class="mt-md-10 mt-sm-8 ma-xs-1 ma-md-1 ma-sm-1 mr-md-2" depressed small color="green" dark>Quick Enquiry <v-icon> mdi-chevron-right</v-icon></v-btn>

          <!-- These 2 buttons needed to be hidden on xs screens, because of space/
          alignment issue. Moreover, they were less important, hence they were choosen
          to be eliminated in xs screens. These 2 buttons together are for a task of
          loginng in or registering for patient portal. To make them look similiar and 
          different from the other 2 buttos, I made them x-small. They were not major 
          tasks for the user, hence did not need a lot of attention, hence they are smaller 
          than the other 2 buttons which were more important !-->
          <div 
            class="d-none d-sm-block"
            elevation="5">
            <v-btn 
            group
            class="mt-md-10 mt-sm-8 ma-xs-auto" x-small color="#711843" dark>Login</v-btn>
            <v-btn class="mt-md-10 mt-sm-8 ma-xs-auto" x-small color="green" dark>Register</v-btn> <!--Button for quick enquiry!-->
          </div>
        </v-col>    
      </v-row>

      <!--Now this part of the code is for the tabs on the toolbar!-->
      <template 
      v-slot:extension> 
      <!-- The tabs are hidden on sm screen size. It looked more cleaner
      and neater by hiding them!-->
        <v-tabs
          v-model="tab"
          align-with-title
          color="#711843"
          class="d-none d-sm-block"

          >
          <!-- 'd-none d-sm-block' is to hide tabs in devices smaller than sm
          The tab slider is given the brand colour. v spacer keeps all the tabs
          aligned to right!-->
          <v-tabs-slider color="#711843"></v-tabs-slider>
          <v-spacer></v-spacer>
          
          <v-tab 
            show-arrows v-for="item in items" :key="item">
            {{ item }}
          </v-tab>

          <!--The code is for the search/magnify button which is only visible on md devices
           d-md-none is the display function which makes the search icon button visible only
           on md devices. the icon colour is the brand's colour. The icon retains focus on the 
           click. On sm device, the icon was sticking to the bottom (the tabs below), hence a 
           margin of 6 pixels to avoid that.!-->
          <div class="d-md-none"> 
            <v-btn
              retain-focus-on-click
              icon color="#711843"
              depressed 
              class=" pa-0 mb-sm-6">
              <v-icon>mdi-magnify</v-icon>
            </v-btn>

            <!--The search text field code!-->
          </div>
          <div class="d-none d-md-block"> <!-- This command hides the search text field on small devices!-->
            <v-text-field
              color="white"
              append-icon="mdi-magnify"
              class="mx-sm-1"
              hide-details="auto"
              label="Search"
              dense
              solo-inverted
            ></v-text-field>
          </div>
        </v-tabs>
      </template>
  </v-toolbar>
</template>


<script>
  export default {
    data () {
      return {
        tab: null,
        items: [
          'Patient Portal', 'Doctors', 'International Patients', 'Outstation OPD',
        ],
        
      }
    },
  }
</script>