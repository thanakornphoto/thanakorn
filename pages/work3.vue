<template>
    <!-- App.vue -->
<v-app>
    <v-system-bar
          color="#1c81ce"
          :height="height"
          :lights-out="lightsOut"
          :window="window"
        >
          <v-spacer></v-spacer>
          <v-icon>mdi-wifi-strength-4</v-icon>
          <v-icon>mdi-signal-cellular-outline</v-icon>
          <v-icon>mdi-battery</v-icon>
          <span>12:30</span>
        </v-system-bar>
  <v-navigation-drawer app>
    <!-- -->
  </v-navigation-drawer>
<div>
     <v-app-bar color="primary"densedark>
            <v-btn icon>
              <v-app-bar-nav-icon></v-app-bar-nav-icon>
            </v-btn>
            <v-toolbar-title>Destinations</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn icon >
              <v-icon>mdi-magnify</v-icon>
            </v-btn>

    </v-app-bar>
</div>
  <!-- Sizes your content based upon application components -->
  <center>
  <img src="../img/n1.jpg" width="250" style="padding-top:50px;">
  <img src="../img/n1.jpg" width="250" style="padding-top:50px;">
  <img src="../img/n1.jpg" width="250" style="padding-top:50px;">
  </center>
  </v-app>
</template>
<script>
export default {
    layout:'de1',
}
</script>