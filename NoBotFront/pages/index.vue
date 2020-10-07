<template>
  

<div>
     <section id='home'>
          <div class='smoothscroll'>
          <v-layout column align-center justify-center class="sub-header">
            <h1
              class="main-header burple  text-xs-center burple"
            >
              You are in control
            </h1>
            <div
              class="subheading text-xs-center burple"
            >
              Know your users are human
            </div>

            <v-btn class="burple rounded-pill padding-btn no-upper"
              dark
              elevation = 24
              ripple = true
              large
              href="https://discord.com/oauth2/authorize?client_id=738360037310726254&permissions=8&scope=bot"
              
              >
              <v-icon class="mr-2">mdi-discord</v-icon> Say hello to NoBot
            </v-btn>
          </v-layout>
        </div>
      </section>

    <v-divider class='divider'></v-divider>


      <section id='setup'>
            <h1
              class="main2-header text-xs-center burple"
            >
            Setup
            </h1>
      <v-container fluid>
      <v-layout row wrap>
            <v-flex sm6>
              <v-card class='align-card-text' height='auto' elevation=10>
                <p class='burple sub-header'>Getting started!</p>
                <v-card-text class='align-card-text'>
                  <p>This’ll probably be short... When NoBot joins your server it automatically create’s everything you need for it to work!</p>

                  <p>All users that were already in your server previously before NoBot was added will be given the “pre-existing” user role, meaning they won’t have to verify themselves and will still have access to channels that they had before.</p>

                  <p>You can edit all the roles NoBot makes just incase you don’t like it, however somethings in the role’s need to be left untouched.</p>
            
                </v-card-text>
              </v-card>
            </v-flex>
            
            <v-flex sm6>
              <v-card class='align-card-text' height='auto' elevation=10>
                <p class='burple sub-header'>Things you can change</p>
                <v-card-text class='burple align-card-text' elevation=10>
                  <p>• The verified user role permissions - Once a user is verified, NoBot no longer limits permissions and gives them regular permissions that you start off with in a normal discord server.</p>

                  <p>• The role colors - NoBot doesn’t discriminate agains’t role colors.</p>

                  <p>• Change nickname - NoBot automatically gives users the permission to change their nickname in the server once verified, this can be turned on/off if you’d like.</p>

                  <p>• TTS (Text To Speach) - NoBot set’s a verified user’s permissions to not be allowed to send a Text To Speach mesage, this can be change on/off, but for the love of god keep it off 😂.</p>
                </v-card-text>
              </v-card>
            </v-flex>
            </v-layout>
      </v-container>

      </section>
      <v-divider class='divider'></v-divider>
            <section id='works'>
            <h1
              class="main2-header text-xs-center burple"
            >
            Get a taste
            </h1>
      <v-container fluid>
      <v-layout row wrap>
            <v-flex lg8 class='center-vid'>
              <v-card class='' elevation=10>
                <v-card-text class='align-card-text'>
                <div style="width:100%;height:0px;position:relative;padding-bottom:56.250%;"><iframe src="https://streamable.com/e/nqnxtm" frameborder="0" width="100%" height="100%" allowfullscreen style="width:100%;height:100%;position:absolute;left:0px;top:0px;overflow:hidden;"></iframe></div>
                </v-card-text>
              </v-card>
            </v-flex>
      
            </v-layout>
      </v-container>

      </section>
  </div>

</template>

<script>
export default {

};
</script>

<style>

html{
  scroll-behavior: smooth !important;
}


.align-card-text{
  text-align: left !important;
  margin-left: 10px !important;
  line-height: 50px !important;
  font-size: 20px !important;
}

.main-header {
  text-align: center !important;
  padding-top: 50px !important;
  padding-bottom: 100px !important;
  font-size: 100px !important;
}

.main2-header {
  text-align: center !important;
  padding-top: 50px !important;
  padding-bottom: 100px !important;
  font-size: 100px !important;
}

.center-vid{
  margin-right: auto;
  margin-left: auto;
}

.no-upper {
  text-transform: none;
}

.burple {
  color: #7289DA;
}

.sub-header {
  font-size: 32px !important;
  font-weight: 500 !important;
}

.padding-btn {
  margin: 150px 50px !important;
  
	-webkit-animation: pulsate-fwd 1s ease-in-out infinite both;
	animation: pulsate-fwd 1s ease-in-out infinite both;
}

.divider {
  padding-top: 200px !important;
  margin-top: 200px !important;
}

@-webkit-keyframes pulsate-fwd {
  0% {
    -webkit-transform: scale(1);
            transform: scale(1);
  }
  50% {
    -webkit-transform: scale(1.1);
            transform: scale(1.1);
  }
  100% {
    -webkit-transform: scale(1);
            transform: scale(1);
  }
}
@keyframes pulsate-fwd {
  0% {
    -webkit-transform: scale(1);
            transform: scale(1);
  }
  50% {
    -webkit-transform: scale(1.1);
            transform: scale(1.1);
  }
  100% {
    -webkit-transform: scale(1);
            transform: scale(1);
  }
}


</style>

