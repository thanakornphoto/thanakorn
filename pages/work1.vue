<template>
<v-app>
    <div>
        <center>
          <h3 style="padding-top:50px;">Welcome!</h3>
          <br>
          <h5>Lorem ipsum dolor sit amet,<br>
          consectetur adipiscing elit.</h5>
          <br>
          <br>
          <br>
          <v-card class="grey lighten-1" style="width: 300px; height: 300px;">
        <img style="position:relative; top:-20px" src ="../img/n1.jpg" width="260" height="340">
        </v-card>
        <br>
        <br>
        <br>
        <br>
        <nuxt-link to="work2"><v-btn style="padding-left:145px;padding-right:145px;"
        @click="doLogin" color="primary" dark large>Sign In</v-btn></nuxt-link>
        </center>

        
    </div>
    </v-app>
</template>
<script>
export default {
      layout:"de1",
}
</script>