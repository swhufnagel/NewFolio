<template>
  <div id="app">
    <font-awesome-icon icon="user-secret" />
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
