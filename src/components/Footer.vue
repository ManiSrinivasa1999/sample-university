<template>
  <div id="footer">
    <v-row
      class="pt-16"
    >
      <template>
        <v-col>
          <div class="red--text pb-6">
            SCHOOLS
          </div>
          <p>
            Business
          </p>
          <p>
            Earth, Energy & Environmental Sciences
          </p>
          <p>
            Education
          </p>
          <p>
            Engineering
          </p>
          <p>
            Humanities & Sciences
          </p>
          <p>
            Law
          </p>
          <p>
            Medicine
          </p>
        </v-col>
        <v-col
          cols="12"
          md="2"
        >
          <div class="red--text pb-4">
            DEPARTMENTS
          </div>
          <p>
            Departments A -to Z
          </p>
          <p>
            Interdisciplinary Programs
          </p>
          <div class="red--text pb-4">
            RESEARCH
          </div>
          <p>
            Research Centers A -to Z
          </p>
          <p>
            Interdisciplinary Research
          </p>
          <p>
            Libraries
          </p>
        </v-col>
        <v-col
          cols="12"
          md="2"
        >
          <div class="red--text pb-4">
            HEALTH CARE
          </div>
          <p>
            Stanford Health Care
          </p>
          <p>
            Stanford Children's Health
          </p>
          <div class="red--text pb-4">
            ONLINE LEARNING
          </div>
          <p>
            Stanford Online
          </p>
        </v-col>
        <v-col
          cols="12"
          md="2"
        >
          <div class="red--text pb-4">
            ABOUT STANFORD
          </div>
          <p>
            Facts
          </p>
          <p>
            History
          </p>
          <p>
            Accreditation
          </p>
          <div class="red--text pb-4">
            ADMISSION
          </div>
          <p>
            Undergraduate
          </p>
          <p>
            Graduate
          </p>
          <p>
            Financial Aid
          </p>
        </v-col>
        <v-col
          cols="12"
          md="2"
        >
          <div class="red--text pb-4">
            RESOURCES
          </div>
          <p>
            A -to Z Index
          </p>
          <p>
            Campus Map
          </p>
          <p>
            Directory
          </p>
          <p>
            Stanford Profiles
          </p>
        </v-col>
        <v-col
          cols="12"
          md="2"
          class=""
        >
          <v-btn
            outlined
            large
            block
            class="pa-4 mb-4"
          >
            Applying
          </v-btn>
          <v-btn
            outlined
            large
            block
            class="pa-4 mb-4 mt-4"
          >
            Visiting
          </v-btn>
          <v-btn
            outlined
            large
            block
            class="pa-4 mb-4 mt-4"
          >
            Giving
          </v-btn>
          <v-btn
            outlined
            large
            block
            class="pa-4 mb-4 mt-4"
          >
            Careers
          </v-btn>
          <v-btn
            outlined
            large
            block
            class="pa-4 mb-4 mt-4"
          >
            Contact
          </v-btn>
        </v-col>
      </template>
    </v-row>
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
  </div>
</template>

<script>
export default {
  data() {
    return {
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
    };
  },
};
</script>

<style lang="scss" scoped>
#footer {
  width: 100% !important;
}
</style>
