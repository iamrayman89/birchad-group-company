<template>
  <div class="py-16">
    <div class="mx-auto text-center" :class="$vuetify.breakpoint.mobile ? 'col-10' : 'col-8' " >
      <h1 class="primary--text">{{ heading }}</h1>
      <p class="mx-auto" :class="$vuetify.breakpoint.mobile ? 'text-left' : '' ">{{ paragraph }}</p>
    </div>
    <v-row class="mx-auto">
      <v-col :cols="$vuetify.breakpoint.mobile ? 12 : 4" v-for="(item, i) in businesses" :key="i">
        <v-card :height="$vuetify.breakpoint.mobile ? '' : '420px'">
          <v-card-text>
            <v-img class="rounded-lg" color="grey ligten-2" height="200" :src="item.image">
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
          </v-card-text>
          <v-card-title>
            <h3 class="primary--text">{{ item.title }}</h3>
          </v-card-title>
          <v-card-subtitle class="secondary--text">{{ item.subtitle }}</v-card-subtitle>
          <v-card-text><p>{{ item.paragraph }}</p></v-card-text>
           <v-card-actions class="hidden-sm-and-up">
            <v-btn text class="secondary--text text-capitalize ">Learn More</v-btn>
           </v-card-actions>

        </v-card>
      </v-col>
    </v-row>

  </div>
</template>

<script>
  export default {
    name: 'Homebusiness',
    data(){
      return{
        heading: 'OUR BUSINESS',
        paragraph: 'Birchand Group, we proudly present our diverse ventures, each driven by a commitment to excellence, innovation, and positively impacting the lives of people and communities.',
        businesses:[
          {
            title:'Cotton',
            subtitle: 'Empowering Rural Livelihoods',
            paragraph: "Cotton is at the heart of Birchand Group's business, representing a significant source of employment and income for approximately 500,000 rural households in Tanzania. ",
            image: require('@/assets/img/cotton.jpg'),

          },
          {
            title:'Autoparts',
            subtitle: 'Driving Efficiency and Reliability',
            paragraph: "The roots of Birchand Group trace back to Gupta Autos Ltd, our first business venture dealing with Scania auto spares and parts. ",
            image: require('@/assets/img/mechanic_hand.jpg'),

          },
          {
            title:'Logistics',
            subtitle: 'Seamless Transportation Solutions',
            paragraph: "Manlax Transporters Ltd, our leading logistics company, stands tall on the route from Dar Es Salaam to the lake region and neighbouring countries like Rwanda and Burundi.",
            image: require('@/assets/img/logistic.jpg'),

          },
          {
            title:'Trading Store',
            subtitle: 'Meeting Diverse Needs',
            paragraph: 'Birchand Trading Store caters to a wide array of products, offering wholesale and retail solutions.',
            image: require('@/assets/img/trading_store.jpg'),

          },
          {
            title:'Real Estate',
            subtitle: 'Building Spaces for Growth',
            paragraph: 'With a keen eye on future development, Birchand Group has invested in Rock Plaza Ltd and Buzuruga Plaza Ltd',
            image: require('@/assets/img/real_estate.jpg'),

          }
        ]

      }
    }
  }
</script>

<style lang="scss" scoped>

</style>
