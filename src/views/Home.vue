<template>
  <div class="home">
    <div
      class="align-center justify-center d-flex flex-column pa-4"
    >
      <span class="text-h2 pa-4 ma-4 font-weight-bold">
        Sample University
      </span>
      <p class="text-h5">
        University students create and apply knowledge by thinking and <br> doing,
        preparing for leadership in a rapidly changing world.
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
        <v-card
          class="mx-auto"
        >
          <v-carousel>
            <v-carousel-item
              v-for="(image,i) in images"
              :key="i"
              :src="image.src"
            ></v-carousel-item>
          </v-carousel>
        </v-card>
      </v-col>
    </v-row>
    <div
      class="align-center justify-center d-flex flex-column pa-4 ma-4"
    >
      <span class="text-h2 pa-4 ma-4 font-weight-bold">
        University News
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
  </div>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {
      images: [
        {
          // eslint-disable-next-line global-require
          src: require('../assets/images/article-1.jpg'),
        },
        {
          // eslint-disable-next-line global-require
          src: require('../assets/images/article-2.jpg'),
        },
        {
          // eslint-disable-next-line global-require
          src: require('../assets/images/article-3.jpg'),
        },
        {
          // eslint-disable-next-line global-require
          src: require('../assets/images/article-4.jpg'),
        },
      ],
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
    };
  },
};
</script>

<style lang="scss" scoped>
.hover-card {
  transition: opacity .4s ease-in-out;
}

.hover-card:not(.on-hover) {
  opacity: 0.8;
 }

</style>
