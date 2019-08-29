<template>
  <nav>
    <v-navigation-drawer v-model="drawer" clipped dark right app>
      <v-list dense>
        <v-list-tile @click="$vuetify.goTo('#landing',
      { offset: 0 })">
          <v-list-tile-action>
            <v-icon>home</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Home</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <v-list-tile @click="$vuetify.goTo('#about',
      { offset: 0 })">
          <v-list-tile-action>
            <v-icon>info</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>About</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <v-list-tile @click="$vuetify.goTo('#skills',
      { offset: 0 })">
          <v-list-tile-action>
            <v-icon>assessment</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Skills</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <v-list-tile @click="$vuetify.goTo('#portfolio',
      { offset: 0 })">
          <v-list-tile-action>
            <v-icon>dashboard</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Portfolio</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <!-- <v-list-tile @click="$vuetify.goTo('#contact',
      { offset: 0 })">
          <v-list-tile-action>
            <v-icon>description</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Resume</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>-->
        <v-list-tile @click="$vuetify.goTo('#contact',
      { offset: 0 })">
          <v-list-tile-action>
            <v-icon>contact_mail</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Contact</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar dark app>
      <v-btn flat @click="$vuetify.goTo('#landing',
      { offset: 5 })">
        <v-toolbar-title id="#myName">Sean Hufnagel</v-toolbar-title>
      </v-btn>
      <v-btn flat @click="$vuetify.goTo('#about',
      { offset: 0 })">About</v-btn>
      <v-btn flat @click="$vuetify.goTo('#skills',
      { offset: 0 })">Skills</v-btn>
      <v-btn flat @click="$vuetify.goTo('#portfolio',
      { offset: 0 })">Portfolio</v-btn>
      <!-- <v-btn flat @click="$vuetify.goTo('#sec5',
      { offset: 0 })">Resume</v-btn>-->
      <v-btn flat @click="$vuetify.goTo('#contact',
      { offset: 0 })">Contact</v-btn>
      <v-spacer></v-spacer>
      <v-toolbar-side-icon fixed right app @click.stop="drawer = !drawer"></v-toolbar-side-icon>
    </v-toolbar>
  </nav>
</template>

<script>
/* eslint-disable */
export default {
  data: () => ({
    drawer: null
  }),
  props: {
    source: String,
    isShrunk: Boolean
  },
  watch: {
    drawer: function(val) {
      console.log(val);
      return val && this.isShrunk === true;
    }
  }
};
</script>

<style scoped>
#myName {
  color: purple;
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif !important;
}
</style>
