<template>
  <div class="award-verification">
    <div
      class="align-center justify-center d-flex flex-column pa-4"
    >
      <span class="text-h2 pa-4 ma-4 font-weight-bold">
        Award Verification
      </span>
      <p class="text-h5 font-weight-bold">
        Search for a La Trobe graduate
      </p>
      <p>
        This search function will find La Trobe graduates from the last 10 years.
      </p>
      <p>
        You can search for a La Trobe graduate by entering the mandatory information
        in either of the search boxes below. It will verify the official course title,<br>
        completion date and conferral (graduation) date.
      </p>
    </div>
    <v-row
      class="fill-height"
      align="center"
      justify="center"
    >
      <v-col
        cols="8"
        md="4"
      >
        <Awardverform1 />
      </v-col>
      <span class="font-weight-bold text-h4">
        OR
      </span>
      <v-col
        cols="8"
        md="4"
      >
        <Awardverform2 />
      </v-col>
    </v-row>
  </div>
</template>

<script>
import Awardverform1 from '@/components/Awardverform1.vue';
import Awardverform2 from '@/components/Awardverform2.vue';

export default {
  name: 'AwardVerification',
  components: {
    Awardverform1,
    Awardverform2,
  },
};
</script>

<style lang="scss" scoped>

</style>
