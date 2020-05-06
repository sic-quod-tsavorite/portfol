<template>
  <v-app>
    <Home />
  </v-app>
</template>

<script>
import Home from "./views/Home";

export default {
  name: "App",
  components: {
    Home
  },

  data: () => ({
    //
  })
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css?family=Fira+Sans|Open+Sans&display=swap");
* {
  font-family: "Fira Sans", sans-serif;
}
</style>