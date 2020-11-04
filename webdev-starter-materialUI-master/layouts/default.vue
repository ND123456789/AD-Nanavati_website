<template>
  <!--Your App Starts Here -->
  <v-app id="banner">
    
    <!--Header -->
     
    <!--<v-app-bar color="purple" dark fixed app>
          <v-toolbar-title>Nanavati</v-toolbar-title>
       <!-- Component Example -->
                
     <Toolbar2/>         
    <!-- Body -->
    <v-content light>
      <chatbot/>
      <nuxt />    
    </v-content>
    

    <!--Code for the footer. The 'app' made the footer not stick to
    the banner. Otherwise it was doing that. Hence, the site's content
    wasnt seen. The 'absolute' made the footer stick to 1 place. Otherwise 
    it was acting like a persistent footer!-->
    <v-footer 
      absolute
      app
      inset
      color="#711843" 
      > 
      <!-- a card was placed before the container. The reason was for
      the grey background. Since, the footer allowed only 1 colour to be 
      applied and I wanted 2 colours that is brand colour and grey colour.
      So, I used the card, applied grey colour to it and tried to fit it 
      through the screen (end to end). Hence, the width is 2000. !-->
      <v-card
        color="grey darken-3"
        flat
        width="2000"
        >
        <v-container>
          <v-row
          align-content-md
          align-content-sm
          >
          <!-- The first row has About us and quick links part of the
          footer. This is coloured in grey. In smaller screen devices,
          each column was placed singly. In the sense, each column occupied
          all the 12 columns. That made the footer content look cleaner and
          neatly organized and also left some breathing space. Hence, xs is 12.!-->
              <v-col
                cols="12"
                sm="6"
                md="6"
                xs="12"
                >
                <h3>About Us</h3>  <!--first row! 1st column-->
                <v-divider></v-divider>
                About Nanavati Hospital<br>
                Leadership<br>
                Newsroom<br>
                Awards<br>
                Community Services<br>
                Privacy Policy<br>
                Terms of Use<br>
                Blogs<br>
              </v-col>
            

              <v-col
                cols="12"
                sm="6"
                md="6"
                xs="12"
                >
                <h3>Quick Links</h3>  <!--first row! 2nd column-->
                <v-divider></v-divider>
                Patient Portal<br>
                STENT pricing<br>
                TKR implant<br>
                Quick Links<br>
                OPD Schedule<br>
                Transplant<br>
              </v-col>
          </v-row>
        </v-container>
      </v-card>
      <v-container>
        <v-row>
          <v-col
            cols="12"
            md="4"
            sm="5"
            xs="12"
            >

            <h3>Stay in touch</h3>  <!--Second row! 1st column-->
            <v-divider></v-divider> <!-- for a thin separating line!-->
              Dr. Balabhai Nanavati Hospital, S.V. Road, Vile Parle (West), Mumbai 400 056, India.<br>
              Tel:+91 22 6836 0000<br>
              24 Hrs helpline: +91 22 2626 7500<br>
              Email:marketing@nanavatihospital.org<br>
          </v-col>
          <v-col
            cols="12"
            md="4"
            sm="3"
            xs="12"
            align="center"
            >
            <h3>Managed by</h3>        <!--Second row! 2nd column-->
            <v-divider></v-divider>
            <br>
            <v-img 
            height="50"
            width="150"
            src="https://www.avendus.com/crypted_storage_img/img_5c20dfec154485.55816330_radient-logos.jpg"></v-img><br>
          </v-col>
          <v-col
            cols="12"
            sm="4"
            md="4"
            xs="12"
            align="right">
            
            <h3>Stay connected</h3>            <!--Second row! 3rd column-->
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