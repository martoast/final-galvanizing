<template>
  <div>

    <section>
      <v-container>
        <div class="py-2" />
        <SectionHeader
          sub-header="About us"
          header="North American Galvanizing LLC"
        />
        <v-row>
          <v-col
            cols="12"
            md="6"
          >
            <h2
              :class="[$vuetify.breakpoint.mdAndUp ? 'display-1' : 'headline']"
              class="mb-4"
            >
              About us<br />
            </h2>

            <p class="subtitle-1">
              North American Galvanizing Industries LLC provides superior
              quality and outstanding service from our staff.

            </p>
            <p class="mb-5">
              Our Galvanizing plant can manage any size project with our two oversized
              kettles measuring 30 ft and 55 ft.

            </p>
            <p class="mb-5">We know how important time is for our clients and due to our high capacity and dedicated team members, our turn around times are fast and efficient with competitive prices with excellent service.

            </p>

            <v-btn
              outlined
              color="primary"
              class="px-5"
              large
              to="/contact"
            >
              Contact Us
            </v-btn>
          </v-col>
          <v-col
            cols="12"
            md="5"
            offset-md="1"
          >
            <v-card class="hidden-sm-and-down">
              <v-img
                :src="this.image"
                height="500"
              >
              </v-img>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <section>

      <VideoSheet />
    </section>
    <section>
      <Contact />
    </section>

  </div>
</template>
<script>
import SectionHeader from "~/components/SectionHeader.vue";
import VideoSheet from "~/components/VideoSheet.vue";
import Contact from "~/components/Contact.vue";
export default {
  head() {
    return {
      title: "#1 SEO Service in Tijuana",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Professional SEO services in Tijuana"
        }
      ]
    };
  },

  layout: "services",

  components: {
    SectionHeader,
    VideoSheet,
    Contact
  },

  data: () => ({
    image: require("~/assets/About.jpg")
  }),

  computed: {}
};
</script>
