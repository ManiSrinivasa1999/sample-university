<template>
  <div
    class="about"
  >
    <div
      class="align-center justify-center d-flex flex-column pa-4"
    >
      <span class="text-h2 pa-4 ma-4 font-weight-bold">
        About University
      </span>
      <p class="text-h5">
        A place for learning, discovery, innovation, expression and discourse
      </p>
    </div>
    <v-row
      class="fill-height"
      align="center"
      justify="center"
    >
      <v-col
        cols="12"
        md="8"
      >
        <v-img src="https://www-media.stanford.edu/wp-content/uploads/2017/03/24182714/about_landing-1.jpg">
        </v-img>
      </v-col>
      <v-col
        cols="12"
        md="8"
      >
        <v-divider></v-divider>
      </v-col>
      <v-col
        cols="12"
        md="8"
        class="d-flex justify-space-between align-center"
      >
        <span class="font-weight-bold text-h6">
          Opened in
        </span>
        <span class="font-weight-bold text-h6">
          Located in
        </span>
        <span class="font-weight-bold text-h6">
          Students
        </span>
        <span class="font-weight-bold text-h6">
          Faculty
        </span>
      </v-col>
      <v-col
        cols="12"
        md="8"
        class="d-flex justify-space-between align-start"
      >
        <span>
          1891
        </span>
        <span>
          Stanford, CA
        </span>
        <span>
          16,424
        </span>
        <span>
          2,219
        </span>
      </v-col>
      <v-col
        cols="12"
        md="8"
      >
        <v-divider></v-divider>
      </v-col>
    </v-row>
     <div
      class="align-center justify-center d-flex flex-column pa-4"
    >
      <span class="text-h2 pa-4 ma-4 font-weight-bold">
        History
      </span>
    </div>
     <v-row
      class="fill-height"
      align="center"
      justify="center"
    >
      <template v-for="(item, i) in items">
        <v-col
          :key="i"
          cols="12"
          md="3"
        >
          <v-hover v-slot:default="{ hover }">
            <v-card
              :elevation="hover ? 12 : 2"
              :class="{ 'on-hover': hover }"
              class="hover-card"
            >
              <v-img
                :src="item.img"
                height="225px"
              >
                <v-card-title class="title white--text">
                  <v-row
                    class="fill-height flex-column"
                    justify="space-between"
                  >
                    <div class="align-self-center">
                      <v-btn
                        v-for="(icon, index) in icons"
                        :key="index"
                        :class="{ 'show-btns': hover }"
                        color="transparent"
                        icon
                      >
                        <v-icon
                          :class="{ 'show-btns': hover }"
                          color="transparent"
                        >
                          {{ icon }}
                        </v-icon>
                      </v-btn>
                    </div>
                  </v-row>
                </v-card-title>
              </v-img>
              <v-card-text
                class="pt-6"
                style="position: relative;"
              >
                <div class="font-weight-light red--text title mb-2">
                  {{ item.title }}
                </div>
                <div class="font-weight-light title mb-2">
                  {{ item.text }}
                </div>
              </v-card-text>
            </v-card>
          </v-hover>
        </v-col>
      </template>
    </v-row>
  </div>
</template>

<script>
export default {
  name: 'About',
  data: () => ({
    items: [
      {
        title: 'UNIVERSITY AFFAIRS',
        text: 'Academic Council discusses resolution regarding climate change',
        img: 'http://lorempixel.com/output/nightlife-q-c-640-480-5.jpg',
      },
      {
        title: 'LAW & POLICY',
        text: 'California’s COVID-19 spike and measures to bend the curve',
        img: 'http://lorempixel.com/output/abstract-q-c-640-480-6.jpg',
      },
      {
        title: 'MEDICINE',
        text: 'Immunotherapy shows potential in treating lung fibrosis',
        img: 'https://images.unsplash.com/photo-1498038432885-c6f3f1b912ee?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=2100&q=80',
      },
    ],
    transparent: 'rgba(255, 255, 255, 0)',
  }),
};
</script>

<style lang="scss" scoped>
</style>
