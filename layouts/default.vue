<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      app
      clipped
      color="gray"
  
    > 
    <v-list>
          <v-list-item>
            <v-list-item-avatar>
              <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John">
            </v-list-item-avatar>

            <v-list-item-content>
              <v-list-item-title>Thanakorn Suntudna</v-list-item-title>
              <v-list-item-subtitle>รักในการเขียน</v-list-item-subtitle>
            </v-list-item-content>

            <v-list-item-action>
              <v-btn
                :class="fav ? 'red--text' : ''"
                icon
                @click="fav = !fav"
              >
                <v-icon>mdi-heart</v-icon>
              </v-btn>
            </v-list-item-action>
          </v-list-item>
        </v-list>
    <v-list-item
            v-for="item in items"
            :key="item.title"
            link
          >
            <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>

            <v-list-item-content>
              <nuxt-link to="/"><v-list-item-title>{{ item.title }}</v-list-item-title></nuxt-link>
              <nuxt-link to="/menu_act"><v-list-item-title>{{ item.titles }}</v-list-item-title></nuxt-link>
              <v-list-item-title>{{ item.title3 }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>


      <lang-selector />
    </v-navigation-drawer>

    <v-app-bar
      app
      clipped-left
      dense
      dark
      src="https://cdn.vuetifyjs.com/images/backgrounds/bg-2.jpg"
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      
      <v-toolbar-title class="mr-12 align-center">
        <span class="title">TECHNICAL CCOLLEGE</span>
      </v-toolbar-title>
      <v-menu offset-y>
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          color="primary"
          dark
          v-bind="attrs"
          v-on="on"
          
        >
          เข้าสู่ระบบ <v-icon dark></v-icon>
        </v-btn>
      </template>
      <v-list>
        <v-list-item
          v-for="(item, index) in itemse"
          :key="index"
          @click=""
        >
          <nuxt-link to="/login"><v-list-item-title>{{ item.title4 }}</v-list-item-title></nuxt-link>
          <nuxt-link to="/register"><v-list-item-title>{{ item.title5 }}</v-list-item-title></nuxt-link>
        </v-list-item>
      </v-list>
    </v-menu>
      <v-spacer></v-spacer>
      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

       <v-btn icon>
        <v-icon>mdi-filter</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-app-bar>

    <v-content>
      <nuxt />
    </v-content>
  </v-app>
</template>

<script>
import LangSelector from '~/components/lang-selector.vue'
export default {
  data: () => ({
      items: [
        { title: 'หน้าหลัก' },
        { titles: 'เช็คกิจกรรม' },
        { title3: 'ตั้งค่า' },
        { title4: 'เข้าสู่ระบบ' },
      ],
       itemse: [
         { title4: 'Login' },
         { title5: 'Register' },
       ],
    }),
  components: {
    data () {
      return {
        drawer: true,
        items: [
          { title: 'Dashboard', icon: 'mdi-view-dashboard' },
          { title: 'Photos', icon: 'mdi-image' },
          { title: 'About', icon: 'mdi-help-box' },
        ],
        color: 'primary',
        colors: [
          'primary',
          'blue',
          'success',
          'red',
          'teal',
        ],
        right: false,
        permanent: true,
        miniVariant: false,
        expandOnHover: false,
        background: false,
      }
    },
    computed: {
      bg () {
        return this.background ? 'https://cdn.vuetifyjs.com/images/backgrounds/bg-2.jpg' : undefined
      },
    },
  },
  computed: {
    drawer: {
      get() {
        return this.$store.state.drawer
      },
      set(v) {
        this.$store.commit('setDrawer', v)
      },
    },
  }, // computed
  watch: {
    '$store.state.lang'() {
      this.$i18n.locale = this.$store.state.lang
    },
  }, // watch
}
</script>