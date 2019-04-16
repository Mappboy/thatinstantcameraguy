<template>
  <v-layout
    column
    justify-center
    align-center
  >
    <v-flex
      xs12
      sm8
      md6
    >
      <div class="text-xs-center">
      </div>
      <cassette />
    </v-flex>
  </v-layout>
</template>

<script>
// https://codepen.io/tomhazledine/pen/IwEDu
// https://codepen.io/kjawhar15/pen/JBreWY
import Cassette from '~/components/Cassette.vue'

export default {
  components: {
    Cassette
  }
}
</script>
