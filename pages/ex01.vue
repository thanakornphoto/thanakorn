<template>
  <div>
    <strong class="white--text text--lighten-1"><h2>Hello: {{ name }}</h2></strong>
    <strong class="blue--text text--lighten-2"><h2>age: {{ age }}</h2></strong>
    <input class="red--text text--lighten-3" type="text" v-model="name">
    <input class="red--text text--lighten-3" type="text" v-model="age">
    <center>
        <br>
        <div><v-btn @click="doSave" small color="primary">SAVE</v-btn></div>
        <p>
        <div><v-btn @click="doMenu" small color="error">MAIN MENU</v-btn></div>
        <p>
        <div><v-btn @click="doHome" small>HOME</v-btn></div>
    </center>
  </div>
</template>
<script>
export default {
  data() {
    return {
      name: "Thanakorn Suntudna",
      age: 19,
    }
  },
  methods:{ //การลิ้งค์
      doSave(){
      console.log("SAVE");
      },
      doMenu(){
          this.$router.push('menu_act')
      },
      doHome(){
          this.$router.push('/')
      }
  }
}
</script>