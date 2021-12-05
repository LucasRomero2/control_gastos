<template>
  <v-app>
    <v-navigation-drawer
      app
      v-model="drawer"
      mini-variant-width="80"
      :expand-on-hover="!this.$vuetify.breakpoint.mdAndDown"
    >
      <side-nav />
    </v-navigation-drawer>

    <v-app-bar app>
      <v-app-bar-nav-icon
        v-if="this.$vuetify.breakpoint.mdAndDown"
        @click="drawer = !drawer"
      />
      <v-toolbar-title>Control de Gastos</v-toolbar-title>
    </v-app-bar>

    <v-main class="app">
      <v-container fluid>
        <router-view></router-view>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import SideNav from "./views/SideNav.vue";
export default {
  components: { SideNav },
  name: "App",
  data: () => ({
    drawer: false,
  }),
  mounted() {
    this.drawer = !this.$vuetify.breakpoint.mdAndDown;
  },
};
</script>

<style scoped>
.app {
  background-color: rgb(221, 221, 221);
}
</style>
