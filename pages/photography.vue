<template>
  <v-container grid-list-xl fluid>
    <v-layout row wrap>
      <vue-instagram token="30983169.96a2602.c96afffd57914aeaa405dde7ca398052" :count=9 mediaType="image">
        <template slot="feeds" slot-scope="props">
          <v-card flat tile>
            <v-img :src="props.feed.link" height="150px"></v-img>
          </v-card>
        </template>
        <template slot="error" slot-scope="props">
          <div class="fancy-alert"> {{ props.error.error_message }} </div>
        </template>
      </vue-instagram>
    </v-layout>
  </v-container>
</template>

<script>
  import VueInstagram from 'vue-instagram'

  export default {
    components: {
      VueInstagram
    }
  }

</script>
