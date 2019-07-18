<template>
  <v-content>
    <div id="sec1"></div>
    <div id="sec2"></div>
    <div id="sec3"></div>
  </v-content>
</template>

<script>
export default {
  data: () => ({
    drawer: null
  }),
  props: {
    source: String
  }
};
</script>

<style scoped>
#sec1 {
  background-image: url("../assets/photos/mePic.jpg");
}
</style>