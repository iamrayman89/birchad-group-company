<template>
  <v-footer
    dark
    padless
  >
    <v-card
      flat
      tile
      class="primary white--text text-center col-12"
    >
     <v-card-text class="white--text">
      <v-row class="mx-auto" justify="center">
        <v-spacer></v-spacer>
        <v-col class="text-start" :cols="$vuetify.breakpoint.mobile  ? 6 : 4" align="start">
      <h2 class="pb-4">Quick Links</h2>
      <div class="my-2 " v-for="(link, i) in links" :key="i">
      <li type="none">
        <a :href="link.path">{{ link.name }}</a>
      </li>
      </div>
        </v-col>
        <v-col align="start" :cols="$vuetify.breakpoint.mobile  ? 6 : 4">
          <h2 class="pb-4">Our Business</h2>
          <div class="my-2" v-for="(business, i) in businesses" :key="i">
          <li type="none">
            <a :href="business.path">{{ business.name }}</a>
          </li>
          </div>
        </v-col>
      </v-row>
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text  d-flex">
        <v-spacer></v-spacer>
      <p><span>&copy; {{ year }} <strong>Birchand Group</strong>. All Rights Reserved </span></p>
        <v-spacer></v-spacer>
      <a :href="icon.path"  target="_black" class="text-decoration-none mx-3 "
      v-for="(icon , i) in icons" :key="i">
        <v-icon large color="secondary" >{{ icon.name }}</v-icon>
      </a>

      </v-card-text>
    </v-card>
  </v-footer>
</template>
<script>
export default {
  name: 'Footer',
  data(){
    return{

      links:[
        {
          name: 'Home',
          path: ''
        },
        {
          name: 'About Us',
          path: ''
        },
        {
          name: 'Our History',
          path: ''
        },
        {
          name: 'Our Future',
          path: ''
        },
      ],
      businesses: [
        {
          name: 'Cotton',
          path: ''
        },
        {
          name: 'Autoparts',
          path: ''
        },
        {
          name: 'Logistics',
          path: ''
        },
        {
          name: 'Trading Store',
          path: ''
        },
        {
          name: 'Real Estate',
          path: ''
        },

      ],



      icons:[
        {
          name: 'mdi-facebook',
          path: ''
        },
        {
          name: 'mdi-instagram',
          path: ''
        },
      ],

    }

  },

    computed:{
    year(){
      return new Date().getFullYear()
    }
  }


}
</script>
<style scoped>
a {
  font-size: 15px;
  line-height: 17px;
  color: white;
  text-decoration: none;
}
a:hover{
  color: #cc1616
}


</style>

