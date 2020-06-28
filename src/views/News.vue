<template>
  <div class="news">
    <div
      class="text-h2 align-center justify-center d-flex pa-4 ma-4 font-weight-bold"
    >
      University News
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
          md="2"
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
    <v-row
      class="fill-height pt-16"
      align="center"
      justify="center"
    >
      <template>
        <v-col cols="12" md="4">
          <v-btn
            x-large
            color="red darken-1"
            dark
            centered
            width="100%"
          >
            More University News
          </v-btn>
        </v-col>
      </template>
    </v-row>
    <v-row
      class="pt-16"
    >
      <template>
        <v-col cols="2"></v-col>
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
        <v-col>
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
        <v-col>
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
        <v-col>
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
        <v-col>
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
        <v-col>
          <v-btn
            outlined
            large
            block
            class="pa-4 ma-4"
          >
            Applying
          </v-btn>
          <v-btn
            outlined
            large
            block
            class="pa-4 ma-4"
          >
            Visiting
          </v-btn>
          <v-btn
            outlined
            large
            block
            class="pa-4 ma-4"
          >
            Giving
          </v-btn>
          <v-btn
            outlined
            large
            block
            class="pa-4 ma-4"
          >
            Careers
          </v-btn>
          <v-btn
            outlined
            large
            block
            class="pa-4 ma-4"
          >
            Contact
          </v-btn>
        </v-col>
        <v-col cols="2"></v-col>
      </template>
    </v-row>
  </div>
</template>

<script>
export default {
  data: () => ({
    icons: ['mdi-rewind', 'mdi-play', 'mdi-fast-forward'],
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
      {
        title: 'LAW & POLICY',
        text: 'Stanford law students help win landmark Supreme Court case',
        img: 'http://lorempixel.com/output/abstract-q-c-640-480-6.jpg',
      },
    ],
    transparent: 'rgba(255, 255, 255, 0)',
  }),
};
</script>

<style>
.hover-card {
  transition: opacity .4s ease-in-out;
}

.hover-card:not(.on-hover) {
  opacity: 0.8;
 }

.show-btns {
  color: rgba(255, 255, 255, 1) !important;
}
</style>
