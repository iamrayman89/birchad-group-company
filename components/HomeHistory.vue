<template>
  <div>
    <v-row class="mx-auto py-16 grey lighten-1">
      <v-col :cols="$vuetify.breakpoint.mobile ? 12: 6 ">
        <v-card>
          <v-img :src="image" color="grey lighten-2">
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
      <v-col class="mx-auto" :cols="$vuetify.breakpoint.mobile ? 12: 5 ">
        <div>
        <h4 class="secondary--text">{{ title }}</h4>
        <v-divider class="secondary" width="110px"></v-divider>
        </div>
        <h1 class="primary--text my-2">{{ heading }}</h1>
        <p class="">{{ paragraph }}</p>
        <v-btn class="secondary mt-3 text-capitalize" to="history">Learn More</v-btn>
      </v-col>
    </v-row>

  </div>
</template>

<script>
  export default {
    name: 'HomeHistory',
    data(){
      return{
        title: 'OUR HISTORY',
        heading: 'The Birchand Group',
        paragraph: "Welcome to the 'Our History' page of Birchand Group, where we take you on a journey through our story of vision, growth, and success.",
        image: require('@/assets/img/birchand_history.jpg')


      }
    }
  }
</script>

<style lang="scss" scoped>

</style>
