<template>
  <div id="app">
    <link
      rel="stylesheet"
      href="https://use.fontawesome.com/releases/v5.2.0/css/all.css"
      integrity="sha384-hWVjflwFxL6sNzntih27bfxkr27PmbbK/iSvJ+a4+0owXq79v+lsFkW54bOGbiDQ"
      crossorigin="anonymous"
    />
    <link
      rel="stylesheet"
      href="https://cdn.rawgit.com/konpa/devicon/df6431e323547add1b4cf45992913f15286456d3/devicon.min.css"
    />

    <v-app>
      <page-header v-bind:isShrunk="isShrunk" />
      <main>
        <v-container fluid v-bind:class="{shrink: isShrunk}">
          <router-view></router-view>
        </v-container>
        <page-footer />
      </main>
    </v-app>
  </div>
</template>

<script>
/* eslint-disable */
import PageHeader from "@/components/Header.vue";
import PageFooter from "@/components/Footer.vue";
export default {
  name: "app",
  data: () => {
    return {
      isShrunk: false
    };
  },
  components: {
    PageHeader,
    PageFooter
  },
  methods: {
    shrinkPage: function() {
      if (isShrunk) {
        viewport.width = "550px";
      }
    }
  }
};
</script>
