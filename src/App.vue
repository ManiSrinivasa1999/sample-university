<template>
  <v-app>
    <v-app-bar
      color="red darken-1"
      dense
      app
      dark=""
      height="75%"
    >
      <v-toolbar-title
        class="text-h4 ml-4 pl-4 font-weight-bold"
      >
        Sample University
      </v-toolbar-title>

      <v-spacer></v-spacer>

      <div v-if="$vuetify.breakpoint.smAndDown">
        <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      </div>
      <div v-else>
        <v-btn
          text
          active-class="red darken-1"
          v-for="button in buttons"
          :key="button.label"
          :to="button.url"
          class="white--text"
        >
          {{ button.label }}
        </v-btn>
      </div>

    </v-app-bar>
     <v-navigation-drawer
      v-if="$vuetify.breakpoint.smAndDown"
      v-model="drawer"
      app
      right
    >
      <v-list dense>
        <v-list-item
          v-for="button in buttons"
          :key="button.label"
          :to="button.url"
          color="red darken-1"
        >
          <v-list-item-content>
            <v-list-item-title>{{ button.label }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <!-- Sizes your content based upon application components -->
    <v-main>
      <!-- Provides the application the proper gutter -->
      <v-container fluid>
        <!-- If using vue-router -->
        <router-view></router-view>
      </v-container>
    </v-main>

    <v-footer>
      <Footer />
    </v-footer>
  </v-app>
</template>

<script>
import Footer from '@/components/Footer.vue';

export default {
  components: {
    Footer,
  },
  data: () => ({
    drawer: null,
    buttons: [
      {
        label: 'Home',
        url: '/',
      },
      {
        label: 'About Us',
        url: '/about',
      },
      {
        label: 'Programmes',
        url: '/programmes',
      },
      {
        label: 'Admissions and Fee',
        url: '/admissions',
      },
      {
        label: 'Award Verification',
        url: '/awardverification',
      },
      {
        label: 'Gallery',
        url: '/gallery',
      },
      {
        label: 'Contact',
        url: '/contact',
      },
      {
        label: 'Apply Now',
        url: '/applynow',
      },
    ],
  }),
};
</script>

<style lang="scss" scoped>
</style>
