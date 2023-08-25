<template>
<div>
    <v-row class="grey lighten-2 mx-auto py-16">
        <v-col class="mx-auto" :cols="$vuetify.breakpoint.mobile ? 12 : 4">
            <div>
                <h4 class="secondary--text">{{ title }}</h4>
                <v-divider class="secondary" width="100px"></v-divider>
            </div>
            <h1 class="primary--text my-2">{{ heading }}</h1>
            <p>{{ Paragraph }}</p>
            <v-btn class="text-capitalize mt-3" to="future" color="secondary">Learn More</v-btn>
        </v-col>
        <v-col class="mx-auto" :cols="$vuetify.breakpoint.mobile ? 12 : 6">
            <v-row>
                <v-col class="" cols="6" v-for="image in images" :Key="image">
                    <v-card>
                        <v-img color="grey lighten-2" :src="image"></v-img>
                    </v-card>
                </v-col>

            </v-row>
        </v-col>

    </v-row>

</div>
</template>

<script>
export default {
    name: 'HomeFuture',
    data() {
        return {
            title: 'OUR FUTURE',
            heading: 'Empowering Growth and Expanding Horizons',
            Paragraph: 'Birchand Group, we share our exciting vision for the coming years and our unwavering commitment to continuous growth, innovation and building a sustainable and prosperous future.',
            images: [
              require('@/assets/img/real_estate.jpg'),
              require('@/assets/img/real_estate.jpg'),
              require('@/assets/img/real_estate.jpg'),
              require('@/assets/img/real_estate.jpg'),
                    ]
        }
    }
}
</script>

<style lang="scss" scoped>

</style>
