<template>
  <div>
    <v-img height="60vh" :src="image" class="pa-0">
    <v-row justify="center" class="mx-auto my-0 fill-height"> 
        <v-col :cols="$vuetify.breakpoint.mobile ? 9 : 3" class="pa-0 mx-auto" :class="backgroundColor">
        <div class="my-16  mx-10" :class="textColor">
        <h4>{{ paragraph }}</h4>
        <h1>{{ heading }}</h1>
        </div>
        </v-col>
      <v-col cols="7"></v-col>

    </v-row>
    </v-img>

  </div>
</template>

<script>
  export default {
    name: 'Hero',
    props: {
      heading: String,
      paragraph: String,
      image: String,
    backgroundColor: String,
      textColor: String
    },
  
  }
</script>

<style lang="scss" scoped>


</style>
