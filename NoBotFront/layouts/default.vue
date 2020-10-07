<template>
  <v-app dark>
    <AppBar />
    <v-container>
      <Appview/>
    </v-container>
  </v-app>
</template>

<script>
import AppBar from "../components/AppBar";
import Appview from "../components/Appview"

export default {
  components: {
    AppBar,
    Appview
  },
  data() {
    return {};
  }
};
</script>
