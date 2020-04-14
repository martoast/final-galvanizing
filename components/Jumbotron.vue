<template>
  <v-sheet
    :height="$vuetify.breakpoint.smAndUp ? '40vh' : '100vh'"
    color="primary"
    tile
  >
    <v-img
      src="https://galco.ie/wp-content/uploads/2016/08/Hot-dip-galvanizing-in-action.jpg"
      aspect-ratio="4.0"
      gradient="to top, rgba(160, 90, 70, .85), rgba(30, 40, 30, .85)"
      height="100%"
    >

      <v-container
        fill-height
        white--text
      >
        <v-slide-x-transition appear>
          <v-col
            align="center"
            justify="center"
          >
            <h1
              :class="$vuetify.breakpoint.smAndUp ? 'display-3' : 'display-2'"
              class="mb-2 font-italic"
              v-text="title"
            />
            <div
              class="title font-weight-light font-italic "
              v-text="subtitle"
            />
          </v-col>

        </v-slide-x-transition>
      </v-container>
      <div class="py-4" />

      <v-row
        class="ma-0"
        justify="center"
        justify-md="start"
      >
        <v-btn
          class="mr-md-3 my-2"
          color="white"
          href="#pricing"
          large
          min-width="175"
          outlined
          rounded
          @click.prevent="$vuetify.goTo('#pricing')"
        >
          Learn More
        </v-btn>

        <v-btn
          class="text--primary my-2"
          color="white"
          href="#try-it"
          large
          min-width="175"
          rounded
          @click.prevent="$vuetify.goTo('#try-it')"
        >
          Sign up
        </v-btn>
      </v-row>
    </v-img>
    <GetAQuote />
  </v-sheet>
</template>

<script>
import GetAQuote from "~/components/GetAQuote.vue";
import VuetifyLogo from "~/components/VuetifyLogo.vue";
export default {
  components: {
    GetAQuote,
    VuetifyLogo
  },
  data: () => ({
    titles: {
      home: {
        title: "Building a Culture of Excellence",
        subtitle: "Vestibulum volutpat pretium libero. Suspendisse eu ligula."
      },
      services: {
        title: "Next Generation Development Today",
        subtitle:
          "Phasellus gravida semper nisi. Fusce convallis metus id felis luctus adipiscing."
      },
      projects: {
        title: "Premium Quality and Branding",
        subtitle: "Vestibulum turpis sem, aliquet eget, lobortis pellentesque."
      },
      contact: {
        title: "Contact Alpha Construction",
        subtitle: "Aenean viverra rhoncus pede. Morbi mollis tellus ac sapien."
      }
    }
  }),

  computed: {
    namespace() {
      if (!this.$route || !this.$route.name) return "";
      return this.$route.name.toLowerCase();
    },

    subtitle() {
      return "Galvanizing industries";
    },
    title() {
      return "North American";
    }
  }
};
</script>
