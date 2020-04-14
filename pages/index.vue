<template>
  <div id="home">
    <v-container id="goals" tag="section">
      <SectionHeader
        header="North American Galvanizing Industries LLC"
        sub-header="Our Services"
      />

      <v-row>
        <v-col
          v-for="(feature, i) in features"
          :key="i"
          class="d-flex"
          cols="12"
          sm="6"
          md="4"
        >
          <v-card outlined max-width="100%">
            <v-img :src="feature.src" height="300" />
            <v-card-title
              class="align-center"
              style="min-height: 88px;"
              v-text="feature.title"
            />
            <v-card-text class="pb-5 pt-3" v-text="feature.text" />
          </v-card>
        </v-col>
      </v-row>
    </v-container>
    <section>
      <VideoSheet />
    </section>
    <section class="pt-6">
      <SectionHeader
        header="North American Galvanizing LLC"
        sub-header="Quality is our Priority"
        text="North American Galvanizing Industries LLC procedures are tracked from customer pick up to delivery, once at our plant stringent quality control measures are followed at every stage of the process. We continue to invest and develop in new technology and procedures to enhance our ability to provide to our customers state of the art galvanizing services."
      />

      <v-container
        id="highlighted-testimonial"
        class="pt-5 px-0 mb-n3"
        fluid
        tag="section"
      >
        <v-parallax
          contain
          src="https://galco.ie/wp-content/uploads/2016/08/Hot-dip-galvanizing-in-action.jpg"
        >
          >
          <v-overlay absolute class="px-3" opacity=".8">
            <testimonial dark :testimonial="highlightedTestimonial" />
          </v-overlay>
        </v-parallax>
      </v-container>
    </section>

    <Contact />
  </div>
</template>

<script>
export default {
  metaInfo: {
    title: "Home",
    meta: [
      {
        name: "description",
        content: "Customized vue-cli templates for Vue and Vuetify"
      }
    ]
  },

  components: {
    Heading: () => import("@/components/Heading"),
    Testimonial: () => import("@/components/Testimonial"),

    SectionHeader: () => import("@/components/SectionHeader"),
    VideoSheet: () => import("@/components/VideoSheet"),
    Contact: () => import("@/components/Contact")
  },

  data: () => ({
    highlightedTestimonial: {
      blurb:
        "Our project at Sony Studios was due on December 26, North American Galvanizing LLC Services was able to provide us with top quality services on 4 days notice even over the holidays, no other provider would even commit to less than three weeks. Their rapid production saved us from a very expensive delay, quality and customer service was top notch. ",
      person: "Luis Robles",
      title: "North American Galvanizing LLC"
    },
    features: [
      {
        title: "Hot Dip:",
        text:
          "Hot-dip galvanizing is the most effective form of galvanizing which involves the process of coating iron and steel with a molting layer of zinc which protects against corrosion.",
        src: require("@/assets/HotDripGalvanizing.jpg")
      },
      {
        title: "Efficiency and Quality",
        text:
          "North American Galvanizing Industries LLC counts with both a 29.6 ft long, 6.7 ft wide and 3.5 ft deep Kettle, and a 55.9 ft long , 4 ft wide and 11.6 ft deep kettle; allowing us to supply galvanizing solutions for your most demanding jobs.",
        src: require("@/assets/Columb2.jpg")
      },
      {
        title: "Where We Operate",
        text:
          "We are based off San Diego County and  Can offer solutions in Santa Clarita, Imperial Valley, Riverside, San Bernardino, Orange County, Los Angeles, Ventura and Santa Barbara Counties.",
        src: require("@/assets/Columb3.jpg")
      }
    ]
  })
};
</script>
<style>
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: 0.5;
  position: absolute;
  width: 100%;
}
</style>
