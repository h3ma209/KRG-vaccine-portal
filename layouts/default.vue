<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      :clipped-left="clipped"
      elevate-on-scroll
      app
      style="background:white"
      class="px-5 "
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      
      
      <v-img src="https://gov.krd/media/1099/govkrdlogobig.svg" height="50" max-width="50" contain class="mx-7"></v-img>
      <v-spacer />
      
    </v-app-bar>
    <v-main>
      <v-container class="fill-height pa-0 ma-0" fluid>
        <nuxt />
      </v-container>
    </v-main>
    <v-navigation-drawer
      v-model="rightDrawer"
      :right="right"
      temporary
      fixed
    >
      
    </v-navigation-drawer>
    <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>

<style scoped lang='scss'>
/* @import url('https://fonts.googleapis.com/css2?family=Noto+Kufi+Arabic:wght@300;400;700&display=swap'); */



html,body{
  
  margin: 0;
  padding: 0;  
}



.v-application{
  font-family: 'Speda', sans-serif !important;
  color: #212a4d !important;
}

.v-application {
  [class*='text-'] {
    color: #36405a;
    font-family: 'Speda', sans-serif !important;
  }
  font-family: 'Speda', sans-serif !important;
}
</style>