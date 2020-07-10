<template>
    <v-form
      ref="form"
      v-model="valid"
      :lazy-validation="lazy"
    >
      <v-text-field
        v-model="username"
        :counter="20"
        :rules="usernameRules"
        label="username"
        required
      ></v-text-field>

            <v-text-field
        v-model="password"
        :counter="20"
        :rules="nameRules"
        label="password"
        required
      ></v-text-field>

      <v-text-field
        v-model="email"
        :rules="emailRules"
        label="E-mail"
        required
      ></v-text-field>

      <v-checkbox
        v-model="checkbox"
        :rules="[v => !!v || 'กรุณากดเพื่อบันทึกรหัสผ่าน!']"
        label="จำรหัสผ่าน?"
        required
      ></v-checkbox>


      <v-btn
        color="error"
        class="mr-4"
        @click="reset"
      >
        ยืนยันการลงทะเบียน
      </v-btn>

      <nuxt-link to="/login"><v-btn
        color="warning"
        @click="resetValidation"
      >
       ยกเลิก
      </v-btn>
      </nuxt-link>
    </v-form>
  </v-row>
</template>