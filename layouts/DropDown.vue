<template>
  <div>
    <v-menu
      open-on-hover>
      <template v-slot:activator="{ on: menu, attrs }">
        <v-btn
          style="font-size: 18px; font-weight: 500"
          color="primary"
          text
          class="text-capitalize"
          elevation="0"
          rounded-lg
          v-bind="attrs"
          v-on="{ ...menu }"
        >
          {{btnText}}
          <!-- <v-icon color="primary" large>mdi-menu-down</v-icon> -->
        </v-btn>
      </template>
      <v-list color="grey" class="pa-6">
        <div class=" text-left">
          <div v-for="(link, i) in links" :key="i" class="my-6">
            <nuxt-link
              class="white--text text-left  mx-6   text-decoration-none"
              :to="link.path">
              <strong class="dropdown">
                 {{link.text }}
              </strong>


              </nuxt-link>

        </div>
        </div>
      </v-list>
    </v-menu>



  </div>
</template>

<script>
export default {
  data() {
    return {
      btnText: 'Our Business',

      links: [
        {
          
          text: "Cotton",
          path: "/international-students",
        },
        {
          
          text: "Autoparts",
          path: "/coming-soon",
        },
        {  
          text: "Logistics",
          path: "/study-abroad",
        },
        {  
          text: "Trading Store",
          path: "/study-abroad",
        },
        {  
          text: "Real Estate",
          path: "/study-abroad",
        },

      ],
    };
  },
};
</script>

<style scoped>

.v-menu__content {
  margin-top: 35px;
  border-radius: 2px;

}
.dropdown{
  color: white;
}
.dropdown:hover {
  color: #da1b1b;

}
a {
  font-size: 17px;
  line-height: 17px;
  text-decoration: none;
  font-weight: 300;
}

</style>
