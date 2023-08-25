<template>
<div>
  <Hero  :heading="hero.heading" :paragraph="hero.paragraph" :image="hero.image" :backgroundColor="hero.color" :textColor="hero.text"/>
  <HomeAbout />
  <HomeHistory />
  <HomeBusiness />
  <HomeFuture />
</div>
</template>

<script>
import Hero from '~/components/Hero.vue'
import HomeAbout from '~/components/HomeAbout.vue'
import HomeBusiness from '~/components/HomeBusiness.vue';
import HomeHistory from '~/components/HomeHistory.vue';
export default {
  components: { Hero, HomeAbout, HomeHistory, HomeBusiness },
  name: 'IndexPage',
  data(){
    return{
      hero: {
        heading: 'BIRCHAND GROUP',
        paragraph: 'Welcome to',
        image: require('@/assets/img/birchand_cotton.jpg'),
        color: 'primary',
        text: 'white--text'
      }
    }
  }
}
</script>
