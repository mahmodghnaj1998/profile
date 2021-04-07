<template>
  <v-app dark>
    <v-navigation-drawer
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
      class="text-center"
    >
      <v-list-item>
        <v-row>
          <v-col cols="12" md="6">
            <v-btn
              :color="$vuetify.theme.dark ? 'blue' : ''"
              block
              large
              @click="dark()"
            >
              Dark
              <v-icon dark right>mdi-weather-night</v-icon>
            </v-btn>
          </v-col>
          <v-col cols="12" md="6">
            <v-btn
              large
              @click="light()"
              :color="$vuetify.theme.dark ? '' : 'blue'"
            >
              Light
              <v-icon dark right>mdi-white-balance-sunny</v-icon>
            </v-btn>
          </v-col>
        </v-row>
      </v-list-item>

      <p class="display-1 mt-4">Mahmod Ghnaj</p>
      <span class="title font-weight-light mb-5"> FullStack Developer</span>
      <v-list>
        <v-list-item v-for="items in items" :key="items.id" class="justify-center">
          <v-list-item-title>  
            <v-btn
              class="text-capitalize subheading font-weight-light mb-3 mt-3"
              text
             @click="$vuetify.goTo(`#${items.fun}`,100)"
            >
              {{ items.title }}
            </v-btn>
          </v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          id: 1,
          title: "About me",
          fun:"about"
        },
        {
          id: 2,
          title: "Services",
          fun:"service"
        },
        {
          id: 3,
          title: "Experience",
          fun:"experience"
        },
        {
          id: 4,
          title: "Skills & Education",
          fun:"skills"
        },
        {
          id:6,
          title:"Project",
          fun:"project"
        },
        {
          id: 5,
          title: "Contact",
          fun:"conect"
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "Vuetify.js",
    };
  },
  methods: {
    dark() {
      this.$vuetify.theme.dark = true;
    },
    light() {
      this.$vuetify.theme.dark = false;
    },
  },
};
</script>
<style >

</style>

