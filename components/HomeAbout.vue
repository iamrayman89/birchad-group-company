<template class="">
  <div class="">
    <v-row class="mx-auto py-16 grey lighten-2">
      <v-col class="mx-auto" :cols="$vuetify.breakpoint.mobile ? 12 : 5">
        <div class="">
        <h5 class="secondary--text">{{ title }}</h5>
        <v-divider class="secondary mt-1" width="65px"/>
        </div>
        <h1 class="my-3 primary--text">{{ heading }}</h1>
        <p>{{ paragraph }}</p>
        <v-btn class="text-capitalize mt-2" to="about" color="secondary">{{ textBtn }} <v-icon>mdi-menu-right</v-icon></v-btn>

      </v-col>
      <v-col :cols="$vuetify.breakpoint.mobile ? 12 : 6">
        <v-card elevation="3">
        <v-img :src="image" color="grey ligten-2">
          <template v-slot:placeholder>
          <v-row
            class="fill-height ma-0"
            align="center"
            justify="center"
          >
            <v-progress-circular
              indeterminate
              color="secondary"
            >
            </v-progress-circular>
          </v-row>
        </template>
        </v-img>
        </v-card>
      </v-col>
    </v-row>

  </div>
</template>

<script>

  export default {
    name: 'HomeAbout',
    data(){
      return{
        title: 'ABOUT US',
        heading: 'A Legacy of Growth and Empowerment',
        paragraph: 'Welcome to Birchand Group, a thriving family-owned business that began its journey in the 1980s under the visionary leadership of Mr. Satpal Aggarwal. We take immense pride in our diverse business lines, which have grown and evolved over the years to touch the lives of many of people across Tanzania and beyond.',
        textBtn: 'Learn More',
        image: require('@/assets/img/birchand_cotton.jpg')
      }
    },
  }
</script>









