<template>
  <div class="awardverform2">
    <v-form
      ref="form"
      v-model="valid"
      lazy-validation
    >
      <span class="font-weight-bold">
        Search by Student Id
      </span>
      <v-text-field
        outlined
        label="Student ID"
        required
        class="mt-4"
      ></v-text-field>

      <v-btn
        color="success"
      >
        Search
      </v-btn>
    </v-form>
  </div>
</template>

<script>
export default {
  name: 'Awardverform2',
};
</script>

<style lang="scss" scoped>

</style>
