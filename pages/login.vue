<template>
  <v-row
    align="center"
    justify="center"
  >
    <v-col cols="12">
      <v-hover
        v-slot:default="{ hover }"
        disabled
      >
        <v-card
          :elevation="hover ? 12 : 2"
          class="mx-auto"
          height="350"
          max-width="350"
          color="#333366"
        >
           <v-card-title class="">
       <h1>เข้าสู่ระบบ!</h1>
     </v-card-title>
     <v-card-text>
       <v-form>
         <v-text-field label="Username" prepend-icon="mdi-account-circle" color="red" />
         <v-text-field 
            :type="showPassword ? 'text' : 'password'" 
            label="Password"
            prepend-icon="mdi-lock"
            color="red"
            :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
            @click:append="showPassword = !showPassword"
          />
         <v-card-actions>
         <nuxt-link to="/register"><v-btn @click="doRegister" color="warning" dark large>สมัครสมาชิก</v-btn></nuxt-link>
          <v-spacer></v-spacer>
         <v-btn @click="doLogin" color="success" dark large>ยืนยัน</v-btn>
         </v-card-actions>
       </v-form>
     </v-card-text>
        </v-card>
      </v-hover>
    </v-col>
  </v-row>
</template>
<script>
export default {
  name: 'App',
  data () {
    return {
      showPassword: false
    }
  }
}
</script>