<template>
  <v-card height="200px">
    <v-bottom-nav
      absolute
      shift
      :value="true"
      :active.sync="e2"
      :color="color"
    >
      <v-btn dark>
        <span>Video</span>
        <v-icon>ondemand_video</v-icon>
      </v-btn>
      <v-btn dark>
        <span>Music</span>
        <v-icon>music_note</v-icon>
      </v-btn>
      <v-btn dark>
        <span>Book</span>
        <v-icon>book</v-icon>
      </v-btn>
      <v-btn dark>
        <span>Image</span>
        <v-icon>image</v-icon>
      </v-btn>
    </v-bottom-nav>
  </v-card>
</template>

<script>
  export default {
    data () {
      return {
        e2: 3
      }
    },

    computed: {
      color () {
        switch (this.e2) {
          case 1: return 'blue-grey'
          case 2: return 'teal'
          case 3: return 'brown'
          case 4: return 'brown lighten-1'
        }
      }
    }
  }
</script>
