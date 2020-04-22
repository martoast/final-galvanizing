<template>
  <div class="text-center">
    <v-dialog
      v-model="dialog"
      fullscreen
    >
      <template v-slot:activator="{ on }">
        <v-btn
          color="white"
          large
          min-width="175"
          outlined
          rounded
          v-on="on"
        >
          <v-icon class="pr-1">mdi-play-circle</v-icon> Watch Video
        </v-btn>
      </template>
      <v-toolbar
        dark
        color="#404b87"
      >
        <v-btn
          icon
          dark
          @click="dialog = false"
        >
          <v-icon>mdi-close</v-icon>
        </v-btn>

      </v-toolbar>

      <div>
        <div align="center">
          <iframe
            style="position:fixed; top:55px; left:0; bottom:0; right:0; width:100%; height:100vh; border:none; margin:0; padding:0; z-index:999999;"
            src="https://bbemaildelivery.com/bbext/?p=vidEmbed&id=2a58e909-da7f-4fe3-aeb2-af8f9144ac8a"
            frameborder="0"
            allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen
            width="100%"
          >

          </iframe>
        </div>
      </div>
    </v-dialog>
  </div>
</template>
<script>
export default {
  data() {
    return {
      dialog: false
    };
  }
};
</script>
