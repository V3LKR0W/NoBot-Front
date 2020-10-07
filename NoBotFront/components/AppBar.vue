<template>
  <div>
    <v-app-bar elevation="10" fixed>
      <v-icon>mdi-all-inclusive</v-icon>

      <v-toolbar-title> {{ title }}</v-toolbar-title>
      <v-spacer />
      <v-btn class='ml-3' v-for="(list, index) in lists" :to="list.to" :key="index">{{
        list.title
      }}</v-btn>
      <v-btn  v-if='button === "🌞"' class='ml-3' @click="$vuetify.theme.dark = !$vuetify.theme.dark, button = '🌝' " 
        > {{ button }} </v-btn>
      <v-btn v-if='button != "🌞"' class='ml-3' @click="$vuetify.theme.dark = !$vuetify.theme.dark, button = '🌞' " 
        > {{ button }} </v-btn>
    </v-app-bar>
    <v-footer
      absolute
      height='auto'
      class='footer'
      elevation="24"
    >
      <v-col
        class="text-center"
        cols="12"
      >
        {{ new Date().getFullYear() }} — <strong>NoBot | <a href='https://crying.world/privacy'>Privacy Policy</a></strong>
      </v-col>
      
    </v-footer>
  </div>
</template>






<script>
export default {
  data() {
    return {
      title: "NoBot",
      button: "🌞",

      lists: [
        {
          title: "Home",
          to: "/#home"
        },
        {
          title: "Setup",
          to: "/#setup"
        },
        {
          title: "Get a taste",
          to: "/#works"
        },
        {
          title: "Report a bug",
          to: "/report-bug"
        },
      ]
    };
  },
  head() {
      return {
        title: 'NoBot ',
      }
      meta: [
          // hid is used as unique identifier. Do not use `vmid` for it as it will not work
          {
            hid: 'description',
            name: 'NoBot',
            content: 'Know your users are human'
          }
        ]
      },
  mounted() {
    const theme = localStorage.getItem("useDarkTheme");
    if (theme) {
      if (theme == "true") {
        this.$vuetify.theme.dark = true;
      } else this.$vuetify.theme.dark = false;
    }
  },
  methods: {
    toggleTheme() {
      this.$vuetify.theme.dark = !$this.vuetify.theme.dark;
      localStorage.setItem("useDarkTheme", this.$vuetify.theme.dark.toString());
    }
  }
  
};

function Dark(){
  $vuetify.theme.dark = !$vuetify.theme.dark
}
function Light(){
  $vuetify.theme.dark = !$vuetify.theme.dark
}



</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');

*{
  font-family: Poppins, sans-serif !important;
}

.footer a{
  text-decoration: none !important;
}

</style>
