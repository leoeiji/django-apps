<template>
  <v-container>
    <v-btn @click="teste">PINTO DO MURILLO TEM 50 CM</v-btn>
  </v-container>
</template>

<script>
export default {
  name: 'IndexPage',

  methods: {
    async teste() {
      let teste = this.$axios
        .$get('/auth/teste', { params: { teste: 123 } })
        .then((r) => {
          console.log(r)
        })
    },
  },
}
</script>
