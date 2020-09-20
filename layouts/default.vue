<template>
  <!--Your App Starts Here -->
  <v-app id="banner">
    
    <!--Header -->
     
    <!--<v-app-bar color="purple" dark fixed app>
          <v-toolbar-title>Nanavati</v-toolbar-title>
       <!-- Component Example -->
                
                  <Toolbar/>
                  
                  
               
         

    <!-- Body -->
    <v-content light>
          <nuxt /> 
          
    </v-content>
    
    <v-footer 
      absolute
      app
      color="grey" 
      > 
      <span class="white--text">&copy; {{ new Date().getFullYear() }}</span>
      <v-container>
        <v-row>
          <v-col
            cols="12"
            sm="4"
            md="3"
            >
            <h3>Home</h3>
            <v-divider></v-divider>
            About Nanavati Hospital<br>
            Leadership<br>
            Newsroom<br>
            Awards<br>
            Community Services<br>
            Sitemap<br>
            Privacy Policy<br>
            Terms of Use<br>
            Blogs<br>
          </v-col>
          <v-col
            cols="12"
            sm="4"
            md="3"
            >
            <h3>Quick Links</h3>
            <v-divider></v-divider>
            Find a Doctor<br>
            Get a Second Opinion<br>
            Treatment and Condition<br>
            Make an Enquiry<br>
            Careers<br>
            Patient Testimonials<br>
            Online Payment<br>
            <h4>Patient Portal</h4>
            <h4>STENT pricing</h4>
            <h4>TKR implant</h4>
          </v-col>
          <v-col
            cols="12"
            sm="4"
            md="3"
            >
            <h3>Quick Links</h3>
            <v-divider></v-divider
            <u>Online Medical records<br></u>
            OPD Schedule<br>
            Feedback<br>
            Transplant data<br></br>

             <h3>Stay in touch</h3>
            <v-divider></v-divider>
            Dr. Balabhai Nanavati Hospital, S.V. Road, Vile Parle (West), Mumbai 400 056, India.<br>
            Tel:+91 22 6836 0000<br>
            24 Hrs helpline: +91 22 2626 7500<br>
            Email:marketing@nanavatihospital.org<br>
          </v-col>

          <v-col
            cols="12"
            sm="4"
            md="3"
            >
            <h3>Stay connected</h3>
            <v-divider></v-divider><br>
            <v-btn icon color="White">
              <v-icon large>mdi-facebook</v-icon>
            </v-btn>
            <v-btn icon color="White">
              <v-icon large>mdi-twitter</v-icon>
            </v-btn>
            <v-btn icon color="White">
              <v-icon large>mdi-youtube</v-icon>
            </v-btn>
            <v-btn icon color="White">
              <v-icon large>mdi-instagram</v-icon>
            </v-btn>
            <v-btn icon color="White">
              <v-icon large>mdi-linkedin</v-icon>
            </v-btn>
          </v-col>
        </v-row>
      </v-container>
    </v-footer>


  </v-app>
</template>

<script>
export default {}
</script>

<style> 
  .black--text {
    border: 1px solid;
  }

   #banner {
    background-color: white;
    colour: black;
  }
</style>