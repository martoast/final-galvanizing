<template>
  <div>

    <!-- <v-row
      justify="center"
      align="center"
    >
      <BigLogo />
    </v-row> -->
    <!-- <v-row
      justify="center"
      align="center"
    >
      <h1 class="mb-4 display-2 text-center">Providing superior quality and Services</h1>
    </v-row> -->

    <v-card
      height="100vh"
      color="transparent"
      class="d-flex pb-12 justify-center"
      flat
      dark
    >
      <v-card
        class="align-self-center"
        color="transparent"
        flat
      >
        <div>
          <v-row justify="center">

            <BigLogo />

          </v-row>
        </div>
        <!-- <div>
          <v-row justify="center">
            <h1 class="mb-4 display-2 text-center">Providing superior quality and Services</h1>

          </v-row>
        </div> -->
        <!-- <h1 class="mb-4 display-2 text-center text--white">Providing superior quality and Services</h1> -->

        <v-row justify="center">
          <v-btn
            class="text--white my-2"
            color="primary"
            x-large
            min-width="245"
            rounded
            @click="$vuetify.goTo('#contact')"
          >Contact us</v-btn>
        </v-row>
        <v-row justify="center">
          <div>
            <VideoDialog />
          </div>
        </v-row>

      </v-card>

    </v-card>

  </div>
</template>
<script>
import BigLogo from "~/components/BigLogo.vue";
import VideoDialog from "~/components/VideoDialog.vue";
export default {
  components: {
    VideoDialog,
    BigLogo
  },
  data: () => ({
    justify: ["center"]
  })
};
</script>
