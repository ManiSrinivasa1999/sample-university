<template>
  <div class="academics">
    <div
      class="align-center justify-center d-flex flex-column pa-4"
    >
      <span class="text-h2 pa-4 ma-4 font-weight-bold">
        Academics
      </span>
      <p class="text-h5">
        Stanford students create and apply knowledge by thinking and <br> doing,
        preparing for leadership in a rapidly changing world.
      </p>
    </div>
    <v-card
      max-width="70%"
      class="mx-auto"
    >
      <v-carousel>
        <v-carousel-item
          v-for="(item,i) in items"
          :key="i"
          :src="item.src"
          reverse-transition="fade-transition"
          transition="fade-transition"
        ></v-carousel-item>
      </v-carousel>
    </v-card>
    <div
      class="align-center justify-center d-flex flex-column pa-4 mt-16 mb-16"
    >
      <span class="text-h2 pa-4 ma-4 font-weight-bold">
        Undergraduate Studies
      </span>
      <v-card
        max-width="70%"
      >
        <v-row>
          <template>
            <v-col
              cols="12"
              md="6"
            >
              <v-img
                :src="items[1].src"
                height="100%"
              >
              </v-img>
            </v-col>
            <v-col
              cols="12"
              md="6"
            >
              <div class="text-h5 font-weight-bold pa-4">
                Undergraduate Education
              </div>
              <p class="pa-2 pl-4">
                Stanford Undergrad is your guide to undergraduate academics and<br>
                opportunities run by the Vice Provost for Undergraduate Education.
              </p>
              <p class="text-h6 pa-2 blue--text pl-4">
                Stanford Undergraduate
              </p>
              <div class="text-h5 font-weight-bold pa-4 pl-4">
                Majors
              </div>
              <p class="pa-2 pl-4">
                Explore the more than 65 major fields of undergraduate study at Stanford.
              </p>

              <p class="text-h6 pa-2 blue--text pl-4">
                Explore Majors
              </p>
              <div class="text-h5 font-weight-bold pa-4">
                Undergraduate Facts & Figures
              </div>
              <p class="pa-2 pl-4">
                Approximately 7,000 undergraduate students attend Stanford.  Learn more<br>
                about the undergraduate program and student body.
              </p>
              <p class="text-h6 pa-2 blue--text pl-4">
                Facts about the Undergraduate Program
              </p>
            </v-col>
          </template>
        </v-row>
      </v-card>
    </div>
    <div
      class="align-center justify-center d-flex flex-column pa-4 mt-64"
    >
      <span class="text-h2 pa-4 ma-4 font-weight-bold">
        Graduate Studies
      </span>
      <v-card
        max-width="70%"
      >
        <v-row>
          <template>
            <v-col
              cols="12"
              md="6"
            >
              <div class="text-h5 font-weight-bold pa-4">
                Office of the Vice Provost for Graduate Education
              </div>
              <p class="pa-2 pl-4">
                The VPGE office works collaboratively acrossthe University to ensure <br>
                that every graduate student has the best possible education.
              </p>
              <p class="text-h6 pa-2 blue--text pl-4">
                Graduate Education
              </p>
              <div class="text-h5 font-weight-bold pa-4 pl-4">
                Graduate Facts & Figures
              </div>
              <p class="pa-2 pl-4">
                Today, more than 9,300 master’s, doctoral, and professional degree students
                are pursuing graduate degrees in all seven of Stanford’s schools.
                Learn more about graduate studies at Stanford.
              </p>

              <p class="text-h6 pa-2 blue--text pl-4">
                Facts about Graduate Studies
              </p>
            </v-col>
            <v-col
              cols="12"
              md="6"
            >
              <v-img
                :src="items[4].src"
                height="100%"
              >
              </v-img>
            </v-col>
          </template>
        </v-row>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          src: 'https://www-media.stanford.edu/wp-content/uploads/2017/03/24182715/academics_landing-1.jpg',
        },
        {
          src: 'https://www-media.stanford.edu/wp-content/uploads/2017/03/09111642/stanford-university-6.jpg',
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
        },
        {
          src: 'https://www-media.stanford.edu/wp-content/uploads/2017/06/23170850/graduate_cars_lab-3x2.jpg',
        },
      ],
    };
  },

};
</script>

<style>

</style>
