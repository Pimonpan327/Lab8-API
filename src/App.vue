<script setup>
import { RouterLink, RouterView } from 'vue-router'
//import HelloWorld from './components/HelloWorld.vue'
</script>
        
<template>
<v-app>
  <v-app-bar :elevation="11"
        color="#2A3B4D"
        theme="dark"
        density="compact"
      >
        <template v-slot:prepend>
          <v-app-bar-nav-icon></v-app-bar-nav-icon>
        </template>

        <v-app-bar-title>Menu</v-app-bar-title>
        <div class="d-flex justify-space-between">
        <!--v-btn variant="text"><routerLink to="/">เข้าสู่ระบบ </routerLink></!--v-btn>-->
        <v-btn variant="text"><RouterLink to="/">Home</RouterLink></v-btn>
        <v-btn variant="text"><RouterLink to="/memes">Memes</RouterLink></v-btn>
        <v-btn variant="text"><RouterLink to="/about">About</RouterLink></v-btn>
        
        </div>

        <template v-slot:append>
          <v-btn icon="mdi-dots-vertical"></v-btn>
        </template>
      </v-app-bar>

    <!--v-navigation-drawer>...</!--v-navigation-drawer>-->

    <v-main>
      <v-container fluid><RouterView /></v-container>
    </v-main>
  </v-app>

</template>
