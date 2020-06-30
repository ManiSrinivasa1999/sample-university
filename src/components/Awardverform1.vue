<template>
  <div class="awardverform1">
    <v-form
      ref="form"
      v-model="valid"
      lazy-validation
    >
      <span class="font-weight-bold">
        Search by last name and date of birth
      </span>
      <v-text-field
        outlined
        label="Name"
        required
        class="mt-4"
      ></v-text-field>

      <v-text-field
        outlined
        label="Last Name"
        required
      ></v-text-field>

      <v-menu
        ref="menu1"
        v-model="menu1"
        :close-on-content-click="false"
        transition="scale-transition"
        offset-y
        max-width="290px"
        min-width="290px"
      >
        <template v-slot:activator="{ on, attrs }">
          <v-text-field
            v-model="dateFormatted"
            label="Date of birth"
            outlined
            v-bind="attrs"
            @blur="date = parseDate(dateFormatted)"
            v-on="on"
          ></v-text-field>
        </template>
        <v-date-picker
          v-model="date"
          no-title
          @input="menu1 = false"
        ></v-date-picker>
      </v-menu>

      <v-btn
        color="error"
        class="mr-4"
      >
        Reset Form
      </v-btn>

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
  name: 'Awardverform1',
  data: (vm) => ({
    date: new Date().toISOString().substr(0, 10),
    dateFormatted: vm.formatDate(new Date().toISOString().substr(0, 10)),
    menu1: false,
  }),
  computed: {
    computedDateFormatted() {
      return this.formatDate(this.date);
    },
  },
  watch: {
    date() {
      this.dateFormatted = this.formatDate(this.date);
    },
  },
  methods: {
    formatDate(date) {
      if (!date) return null;
      const [year, month, day] = date.split('-');
      return `${month}/${day}/${year}`;
    },
    parseDate(date) {
      if (!date) return null;
      const [month, day, year] = date.split('/');
      return `${year}-${month.padStart(2, '0')}-${day.padStart(2, '0')}`;
    },
  },

};
</script>

<style lang="scss" scoped>

</style>
