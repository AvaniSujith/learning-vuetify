<template>
  <v-app class="rounded rounded-md border">
    <!-- <v-app-bar title="Application bar">
    </v-app-bar> -->
    <v-toolbar density="compact">
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <v-toolbar-title>
        <router-link to="/">Vuetify</router-link>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        to="/login"
        variant="outlined"
        size="small"
        color="pink-darken-4"
        text="Login"
      ></v-btn>
    </v-toolbar>
    <v-main>
      <v-container fluid>
        <RouterView />
      </v-container>
    </v-main>
  </v-app>
</template>
