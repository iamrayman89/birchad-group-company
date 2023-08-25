<template>
    <div>
        <Hero :backgroundColor="hero.color" :heading="hero.heading" :image="hero.image" :paragraph="hero.paragraph" :textColor="hero.text" />
        <v-row class="py-16">
            <v-col class="text-center">
                <div class="primary--text">
                
                <h1>A Legacy of Growth</h1>
                </div>
                <p class="mx-auto col-10 text-left">The story of Birchand Group is a testament to the power of vision, dedication, and innovation. With Mr. Satpal Aggarwal's founding inspiration and Mr. Manish Aggarwal's forward-thinking leadership, Birchand Group continues to thrive in a dynamic and ever-changing business landscape. Our journey doesn't end here; we are committed to embracing new opportunities, serving our customers with excellence, and making a positive impact in the industries we operate.
Join us as we build on our legacy of growth, driven by our founder's vision and our CEO's unwavering commitment to progress. Together, we will forge a future filled with success, prosperity, and a relentless pursuit of excellence.
</p>

            </v-col>
        </v-row>

    </div>
</template>

<script>
import Hero from '~/components/Hero.vue'
    export default {
  components: { Hero },
        name: 'history',
        data(){
            return{
                hero:{
          color: 'grey lighten-1',
          text: 'white--text',
          heading: 'Where Vision Drives Success',
          paragraph: 'Birchand Group ',
          image: require('@/assets/img/ginnely.jpg')


        },

            }

        }
    }
</script>

<style lang="scss" scoped>

</style>