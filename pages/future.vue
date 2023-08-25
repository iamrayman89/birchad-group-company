<template>
<div>
    <Hero :backgroundColor="hero.color" :heading="hero.heading" :image="hero.image" :paragraph="hero.paragraph" :textColor="hero.text" />
    <v-row class="grey lighten-1 mx-auto py-16">
        <v-col class="mx-auto" cols="4" v-for="(item, i) in future" :key="i">

            <h1 class="primary--text my-3">{{ item.heading }}</h1>
            <p class="">{{ item.paragraph }}</p>

        </v-col>

    </v-row>
    <v-row class="mx-auto py-16">
        <v-col cols="12" class="text-center">
            <div class="mx-auto col-8">
                <h1 class="primary--text my-4">{{ product.heading }}</h1>
                <p>{{ product.paragraph }}</p>
            </div>
        </v-col>
        <v-col cols="6" v-for="(item, i) in products" :key="i">
            <v-card height="400" class="d-flex" :class="i%2 == 0 ? 'flex-row' : 'flex-row-reverse'">
                <v-card-text>
                    <v-avatar tile size="300" height="360">
                        <v-img class="rounded-lg" height="" :src="item.image"></v-img>
                    </v-avatar>
                </v-card-text>
                <div class="d-inline-block">
                    <v-card-title>
                        <h3 class="primary--text">{{ item.heading }}</h3>
                    </v-card-title>
                    <v-card-subtitle class="secondary--text" >{{ item.subtitle }}</v-card-subtitle>
                    <v-card-text>{{ item.paragraph }}</v-card-text>
                </div>

            </v-card>
        </v-col>
    </v-row>
</div>
</template>

<script>
import Hero from '~/components/Hero.vue'
export default {
    components: {
        Hero
    },
    name: 'Future',
    data() {
        return {
            image: require('@/assets/img/sunset.jpg'),

            hero: {
                color: 'primary',
                text: 'white--text',
                paragraph: 'Welcome to the Future of Birchand Group ',
                heading: 'A Journey of Growth and Sustainability!',
                image: require('@/assets/img/sunset.jpg')
            },
            future: [{
                    heading: 'Continuing the Legacy',
                    paragraph: "Since our inception in 1990, Birchand Group has remained steadfast in upholding the values of integrity, innovation, and customer satisfaction. As we look ahead, we are determined to build on the strong foundation laid by Mr. Satpal Aggarwal. His entrepreneurial spirit and foresight have driven our growth and success, and we will carry his legacy forward with pride and dedication.",
                },
                {
                    heading: 'The MUB Facility',
                    paragraph: "As the only company in Tanzania with an inland Manufacture Under Bond (MUB) facility, Birchand Group enjoys a distinctive advantage in the industry. This facility allows us to import inputs tax-exempt and pay taxes only on the final products. This strategic advantage significantly reduces our initial capital outlay on production and processing, enabling us to enhance efficiency and deliver cost-effective products to our valued customers."
                },

            ],
            product: {
                heading: 'Expanding Our Product Portfolio',
                paragraph: "At Birchand Group, we have always embraced a forward-looking approach, focused on expanding our product portfolio to cater to evolving market demands. In the near future, we have identified two key products that will become integral to our offerings:"
            },
            products: [{
                    heading: 'Soap',
                    subtitle: 'A Sustainable Vision',
                    paragraph: "In 2024, Birchand Group embarks on an exciting journey to produce soap for the Tanzanian domestic market. This strategic move is driven by our commitment to sustainability and resource optimization. With sludge, a by-product obtained during the oil extraction process, accounting for 63% of the soap's raw material, we are dedicated to making the most of our resources and reducing waste.",
                    image: require('@/assets/img/sunset.jpg')
                },
                {
                    heading: 'Cotton Yarn ',
                    subtitle: 'A Value-Add Proposition',
                    paragraph: "In 2025, we are thrilled to introduce cotton yarn to our product portfolio. As experts in the cotton lint export market, adding cotton yarn to our offerings is a natural progression for Birchand Group. This value-add process will enhance the utility and versatility of our cotton lint products. One unique aspect of Birchand cotton yarn will be our ability to export it to Asia, positioning us as the sole company in East Africa to do so.",
                    image: require('@/assets/img/sunset.jpg')
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

</style>
