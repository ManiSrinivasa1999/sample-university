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
          active-class="red"
          v-for="button in buttons"
          :key="button.label"
          :to="button.url"
          color="red darken-1"
          class="white--text ma-1"
        >
          {{ button.label }}
        </v-btn>
        <v-btn
          color="red darken-1"
          class="white--text ma-1"
        >
          Search
          <v-icon right dark>mdi-magnify</v-icon>
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

    <v-footer
      padless
    >
      <v-card
        flat
        tile
        class="red darken-1 lighten-1 white--text text-center flex"
      >
        <v-card-text
          class="red lighten-5"
        >
          <v-btn
            v-for="icon in icons"
            :key="icon.icon"
            :href="icon.url"
            class="mx-4 white--text"
            icon
            target="_blank"
          >
            <v-icon
              x-large
              :color="icon.color"
            >
              {{ icon.icon }}
            </v-icon>
          </v-btn>
        </v-card-text>

        <v-divider></v-divider>
        <v-card-text class="white--text">
          {{ new Date().getFullYear() }} — <strong>Manisrinivasa</strong>
        </v-card-text>
      </v-card>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    drawer: null,
    icons: [
      {
        icon: 'mdi-facebook',
        url: 'https://www.facebook.com/manisrinivas.badam/',
        color: '#3b5998',
      },
      {
        icon: 'mdi-twitter',
        url: 'https://twitter.com/Manisrinivas15',
        color: '#00acee',
      },
      {
        icon: 'mdi-linkedin',
        url: 'https://www.linkedin.com/in/badam-manisrinivasa-narayana-5637a2176/',
        color: '#0e76a8',
      },
      {
        icon: 'mdi-github',
        url: 'https://github.com/Manisrinivasa1999',
        color: '#211F1F',
      },
    ],
    buttons: [
      {
        label: 'News',
        url: '/news',
      },
      {
        label: 'Events',
        url: '/events',
      },
      {
        label: 'Academics',
        url: '/academics',
      },
      {
        label: 'Research',
        url: '/research',
      },
      {
        label: 'Health care',
        url: '/healthcare',
      },
      {
        label: 'Campus Life',
        url: '/campuslife',
      },
      {
        label: 'Admission',
        url: '/admission',
      },
      {
        label: 'About',
        url: '/about',
      },
    ],
    tabs: [
      {
        label: 'Students',
        url: '/students',
      },
      {
        label: 'Faculty & Staff',
        url: '/facultyandstaff',
      },
      {
        label: 'Parents',
        url: '/parents',
      },
      {
        label: 'Vistors',
        url: '/vistors',
      },
      {
        label: 'Alumni',
        url: '/alumni',
      },
    ],
  }),
};
</script>

<style lang="scss">
</style>
