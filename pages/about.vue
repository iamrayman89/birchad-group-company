<template>
<div>
    <Hero :backgroundColor="hero.color" :heading="hero.heading" :image="hero.image" :paragraph="hero.paragraph" :textColor="hero.text" />
    <v-row class="py-16 mx-auto grey lighten-1">
        <v-col class="mx-auto" :cols="$vuetify.breakpoint.mobile ? 12 : 5">
            <h1 class="primary--text my-4">{{ heading }}</h1>
            <p>{{ paragraph }}</p>

        </v-col>
        <v-col :cols="$vuetify.breakpoint.mobile ? 12 : 6">
            <v-card class="">
                <v-img height="400px" :src="image"></v-img>
            </v-card>
        </v-col>
    </v-row>
    <v-row class="mx-auto py-16">
        <v-col :cols="$vuetify.breakpoint.mobile ? 12 : 6" v-show="$vuetify.breakpoint.mobile ? false : true">
            <v-row>
                <v-col cols="6">
                    <v-card>
                        <v-img height="200" :src="image"></v-img>
                    </v-card>
                </v-col>
                <v-col cols="6">
                    <v-card>
                        <v-img height="200" :src="image"></v-img>
                    </v-card>
                </v-col>
                <v-col cols="12">
                    <v-card>
                        <v-img height="300" :src="image"></v-img>
                    </v-card>
                </v-col>
            </v-row>

        </v-col>
        <v-col class="mx-auto" :cols="$vuetify.breakpoint.mobile ? 12 : 5">
            <v-row class="mx-auto" v-for="(detail, i) in details" :key="i">

                <h2 class="primary--text my-2"> {{ detail.heading }}</h2>
                <p>{{ detail.paragraph }}</p>
                <v-img :src="detail.image" v-show="$vuetify.breakpoint.mobile ? true: false " ></v-img>
                
            </v-row>
        </v-col>
    </v-row>
    <v-row justify="center" class="py-16 mx-auto grey lighten-2">
        <v-col cols="12" class="center-text">
            <h1 class="primary--text text-center">Core Values</h1>
        </v-col>
        <v-col :cols="$vuetify.breakpoint.mobile ? 12 : 5" class="" v-for="(item, i) in cores" :key="i">
            <v-card class="  rounded-lg" :height="$vuetify.breakpoint.mobile ? '' : 350 ">
                <v-avatar class="ma-4" size="100" tile>
                    <v-img class="rounded" :src="image"></v-img>
                </v-avatar>

                <v-card-title>
                    <h4>{{ item.heading }}</h4>
                </v-card-title>
                <v-card-text class=""><i>{{ item.paragraph }}</i></v-card-text>
            </v-card>

        </v-col>
    </v-row>

</div>
</template>

<script>
import Hero from '~/components/Hero.vue'
export default {
    name: 'about',
    components: {
        Hero
    },
    data() {
        return {
            hero: {
                color: 'secondary',
                text: 'white--text',
                heading: 'About Us',
                paragraph: 'Get to know',
                image: require('@/assets/img/real_estate.jpg')

            },
            heading: "Our Founder's Vision",
            paragraph: "At the heart of Birchand Group lies the vision of our founder, Mr. Satpal Aggarwal. With a humble start in the auto spares industry, he possessed the foresight and determination to explore new opportunities and expand our horizons. In 1994, he took a significant step by venturing into the agricultural sector, focusing on cotton in Mwanza and the greater Lake region. This decision marked the inception of Birchand Oil Mill Ltd, one of the earliest players in the Tanzanian cotton sector.",
            image: require('@/assets/img/birchand_tree.jpg'),

            details: [{
                    heading: 'A Full Value Chain',
                    paragraph: "Birchand Group's dedication to excellence and continuous growth is evident through our successful establishment of a full value chain in the cotton industry. From purchasing and collecting raw cotton to meticulous cleaning, ginning, sorting, and further processing, we ensure that each step is executed with precision. This meticulous approach has led us to produce an array of products, including cotton lint, cotton seed oil, cakes, and husks."
                },
                {
                  image: require('@/assets/img/cotton.jpg')

                },
                {
                    heading: 'Pioneering Logistics Solutions',
                    paragraph: "Driven by the need to transport cotton products efficiently across Tanzania, Mr. Satpal Aggarwal identified an opportunity to streamline the operations further. Thus, the sister company, Manlax Transporters Ltd, was born. With our own fleet of trucks, we seamlessly facilitate the movement of cotton, minimizing transport costs and optimizing the supply chain."
                }, 
                {
                  image: require('@/assets/img/cotton.jpg')

                },

            ],

            cores: [{
                    heading: 'Empowering Lives',
                    paragraph: 'Beyond our business success, Birchand Group takes immense pride in the positive impact we have made in countless lives. Through direct and indirect employment opportunities, we have reached people in even the most remote areas of Tanzania. Our commitment to fostering growth and empowering communities extends beyond business profits, and it remains an integral part of our ethos.',
                },
                {
                    heading: 'A Leading Market Presence',
                    paragraph: 'Through tireless efforts and a commitment to excellence, Birchand Group has emerged as one of the largest cotton buyers in Tanzania, enjoying an impressive 30% market share. Our dedication to quality, reliability, and customer satisfaction has earned us a strong reputation within the industry.',
                },
                {
                    heading: 'Our Promise for the Future',
                    paragraph: "As we reflect on our journey, we are filled with gratitude for the trust our customers and partners have placed in us. Birchand Group remains committed to nurturing our founder's vision of growth and diversification. We will continue exploring new opportunities and expanding into new business lines to contribute positively to the economic landscape of Tanzania.",
                },
                {
                    heading: 'Join Us in the Journey',
                    paragraph: 'We extend our heartfelt gratitude to all those who have been a part of our journey, and we invite you to join us as we forge ahead, creating a future that is built on the foundation of innovation, integrity, and empowerment. Together, we will continue to make a difference in the lives of people, businesses, and communities.',
                },
            ]
        }

    }
}
</script>

<style lang="scss" scoped>

</style>
