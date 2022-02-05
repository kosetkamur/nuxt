<template>
  <v-row style="justify-content: left">
    <v-btn color="lighten-2 ma-5" @click="dialog = !dialog">
      Форма для заполнения
    </v-btn>
    <v-col cols="10" v-if="dialog">
      <formForAnimals @close="dialog = !dialog"></formForAnimals>
    </v-col>

    <v-row>
      <v-col cols="6" md="4" sm="6" v-for="animal in animals" :key="animal.id">
        <spisok :animal="animal" />
      </v-col>
    </v-row>
  </v-row>
</template>

<script>
import { mapGetters } from 'vuex'
export default {
  data: () => ({
    dialog: false,
  }),
  computed: {
    ...mapGetters({
      animals: 'animals/getAminals',
    }),
  },
  async mounted() {
    this.$store.dispatch('form/getData')
    this.$store.dispatch('animals/getAnimals')
  },
}
</script>
