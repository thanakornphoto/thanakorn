<template>
  <v-container fluid class="pa-0">
    <v-row align="center">
      <v-col cols="12" sm="6">
        <div class="text-center">
          <div class="my-2">
            <nuxt-link to="/activity/flag"><v-btn x-large color="secondary" dark>กิจกรรมหน้าเสาธง</v-btn></nuxt-link>
          </div>
          <div class="my-2">
            <nuxt-link to="/activity/line"><v-btn x-large color="primary" dark>กิจกรรมเข้าแถว</v-btn></nuxt-link>
          </div>
          <div class="my-2">
            <nuxt-link to="/activity/homeroom"><v-btn x-large color="warning" dark>กิจกรรมโฮมรูม</v-btn></nuxt-link>
          </div>
          <div class="my-2">
            <nuxt-link to="/activity/special"><v-btn x-large color="success" dark>กิจกรรมพิเศษ/จิตอาสา</v-btn></nuxt-link>
          </div>
        </div>
      </v-col>
      <v-col cols="12" sm="6">
        <div class="text-center">
          <div class="my-2">       
            <v-btn color="error" fab x-large dark>
              <nuxt-link to="/"><v-icon>mdi-arrow-left</v-icon>
              </nuxt-link>
            </v-btn>
          </div>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>