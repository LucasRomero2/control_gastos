<template>
  <v-list>
    <v-list-item class="px-2">
      <v-list-item-avatar tile>
        <v-img src="../assets/logo.svg"></v-img>
      </v-list-item-avatar>
      <v-list-item-title class="text-h6">
        Nombre de la app logo
      </v-list-item-title>
    </v-list-item>

    <v-divider></v-divider>

    <v-list dense nav>
      <v-list-item
        v-for="item in items"
        :key="item.title"
        link
        :style="{
          'padding': '10px 5px',
          'margin-top': '20px',
        }"
      >
        <v-list-item-icon my-auto>
          <v-icon size="30">{{ item.icon }}</v-icon>
        </v-list-item-icon>

        <v-list-item-content>
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-list>
</template>

<script>
export default {
  name: "SideNav",
  data: () => ({
    items: [
      { title: "Principal", icon: "mdi-home-outline" },
      { title: "Movimientos", icon: "mdi-format-list-bulleted" },
      { title: "Presupuestos", icon: "mdi-flag-outline" },
      { title: "Cuentas", icon: "mdi-bank-outline" },
      { title: "Informes", icon: "mdi-chart-line" },
      { title: "Configuración", icon: "mdi-cog-outline" },
    ],
  }),
};
</script>