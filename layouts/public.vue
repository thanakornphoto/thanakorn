<template>
<v-app>
  <v-card>
        <v-system-bar dark color="drak">
      <v-spacer></v-spacer>
      <v-icon>mdi-wifi-strength-4</v-icon>
      <v-icon>mdi-signal-cellular-outline</v-icon>
      <v-icon>mdi-battery</v-icon>
      <span>12:30</span>
    </v-system-bar>
    <v-toolbar
      color="pink lighten-1"
      dark
      flat
    >
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>INFORMATION</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>

      <template v-slot:extension>
        <v-tabs
          v-model="tab"
          align-with-title
        >
          <v-tabs-slider color="yellow"></v-tabs-slider>

          <v-tab v-for="item in items" :key="item">
            {{ item }}
          </v-tab>
        </v-tabs>
      </template>
    </v-toolbar>

    <v-tabs-items v-model="tab">
      <v-tab-item
        v-for="item in items2"
        :key="item,i"
        
      >
        <v-card flat>
          <v-card-text v-text="text"></v-card-text>
        </v-card>
      </v-tab-item>
      <!-- ใส่ข้อความ -->
  <v-main>
    <v-container fluid>
     <v-content>
       <nuxt/>
     </v-content>
    </v-container>
  </v-main>
      <v-bottom-navigation
    :value="activeBtn"
    color="pink lighten-1"
    horizontal
  >
    <v-btn>
      <span>Recents</span>
      <v-icon>mdi-history</v-icon>
    </v-btn>

    <v-btn>
      <span>Favorites</span>
      <v-icon>mdi-heart</v-icon>
    </v-btn>

    <v-btn>
      <span>Nearby</span>
      <v-icon>mdi-map-marker</v-icon>
    </v-btn>
  </v-bottom-navigation>
    </v-tabs-items>
  </v-card>
  </v-app>
</template>
<script>
  export default {
    data () {
      return {
        tab: null,
        items: [
          'ประวัติส่วนตัว',],
        items2: [
          'shopping', 'videos',
          ],
      }
    },
  }
</script>
