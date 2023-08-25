<template>
  <v-app dark>

    <v-app-bar
    class="white"
    :height="$vuetify.breakpoint.mobile ? '60px': '90px'"
    elevation="2"
     dense
     hide-on-scroll
     app
     >

      <v-toolbar-title>
        <nuxt-link class="primary--text" to="/">
      <v-img class="" width="400px" :src="image"></v-img>
        </nuxt-link>
      </v-toolbar-title>
      <v-spacer />
       
      <div   dark class="hidden-sm-and-down pa-3" plain>
        <nuxt-link class="primary--text" to="about">About</nuxt-link>
      </div>
      <div   dark class="hidden-sm-and-down pa-3" plain>
        <nuxt-link class="primary--text" to="history">Our History</nuxt-link>
      </div>

      <div  dark class="hidden-sm-and-down pa-3" plain>
        <DropDown />
      </div>
      <div   dark class="hidden-sm-and-down pa-3" plain>
        <nuxt-link class="primary--text" to="future">Our Future</nuxt-link>
      </div>
      <v-spacer />
      <v-btn class="primary mx-6 hidden-sm-and-up" icon @click.stop="rightDrawer = !rightDrawer">
        <v-icon color="white">mdi-menu</v-icon>
      </v-btn>
    </v-app-bar>
    <v-main>
      <div>
        <Nuxt />
      </div>
    </v-main>
    <v-navigation-drawer
    v-model="rightDrawer"
     :right="right"
     temporary
     fixed>
     <v-toolbar-title>
        <nuxt-link class="primary--text" to="/">
      <v-img class="" width="400px" :src="image"></v-img>
        </nuxt-link>
      </v-toolbar-title>
      <v-list>
        <v-list-item
           v-for="(item, i) in items"
          :key="i"
          :to="item.destination"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <Footer />
  </v-app>
</template>

<script>
import DropDown from './DropDown.vue'
import Footer from './Footer'
export default {
  name: 'DefaultLayout',
  components:{ Footer, DropDown},
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [

        {
          icon: 'mdi-chart-bubble',
          title: 'About Us',
          destination: '/about',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Our History',
          destination: '/history',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Our Future',
          destination: '/future',
        },
      ],
      media:[
        {
          name: 'mdi-facebook',
          path: '',
        },
        {
          name: 'mdi-instagram',
          path: '',
        },
        {
          name: 'mdi-twitter',
          path: '',
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'BIRCHAND GROUP',
      image: require('@/assets/img/logo.png')
    }
  },
}
</script>

<style>
* {
  font-family: "Open Sans", sans-serif;

}
body{
  font-family: "Open Sans", sans-serif;
  color: #444444;

}
 .v-application a {
  text-decoration: none;

 }
 a {
  font-size: 17px;
  line-height: 17px;
  text-decoration: none;
  font-weight: 500;
}


h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: "Raleway", sans-serif;
}

</style>
