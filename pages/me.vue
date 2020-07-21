<template>
  <v-card
    class="mx-auto"
    max-width="400"
  >
    <v-img
      class="white--text align-end"
      height="350px"
      src="https://scontent.fbkk22-2.fna.fbcdn.net/v/t1.0-9/68631380_2088251108145482_1787979728385212416_o.jpg?_nc_cat=106&_nc_sid=8bfeb9&_nc_eui2=AeEUS7Zg03qksIxOlYz0HUZ_B28faziGQf0Hbx9rOIZB_TNc9LeMW4nagGzHqnh-vHzhwb4YiIBCUivOyN9PeMVn&_nc_ohc=oVWhDBUSxcMAX_VTNy4&_nc_ht=scontent.fbkk22-2.fna&oh=384cfdd8c2b9f68510f45a8392935fd5&oe=5F3B7EC6"
    >
      <v-card-title class="red">Thanakorn Suntudna</v-card-title>
    </v-img>

    <v-card-subtitle class="pb-0">Number 10</v-card-subtitle>

    <v-card-text class="text--primary">
      <div>Information technology</div>

      <div>25, Moo9 Niwetrat Kangsanamnung 30440</div>
    </v-card-text>

    <v-card-actions>
      <v-btn
        color="blue"
        text
      >
        LIKE
      </v-btn>

      <v-btn
        color="red"
        text
      >
        Share
      </v-btn>
      <v-chip
      class="ma-2"
      color="orange"
      outlined
      pill
    >
      Follow me
      <v-icon right>mdi-account-outline</v-icon>
    </v-chip>
    </v-card-actions>
  </v-card>
</template>
<script>
export default {
   layout:'public',
  name: 'App',
  data () {
    return {
      showPassword: false
    }
  }
}
</script>