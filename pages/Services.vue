<template>
  <div>
    <v-container
      id="goals"
      tag="section"
    >
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
          <v-card
            outlined
            max-width="100%"
          >
            <v-img
              :src="feature.src"
              height="300"
            />
            <v-card-title
              class="align-center"
              style="min-height: 88px;"
              v-text="feature.title"
            />
            <v-card-text
              class="pb-5 pt-3"
              v-text="feature.text"
            />
          </v-card>
        </v-col>
      </v-row>
    </v-container>
    <section
      id="services"
      class="py-5"
    >
      <!-- <SectionHeader
        header="North American Galvanizing Industries LLC"
        sub-header="Explore our Services"
      /> -->

      <v-container>
        <v-row
          align="center"
          class="mb-5"
        >
          <v-col
            cols="12"
            md="4"
          >
            <v-card outlined>
              <client-only>
                <v-img
                  :src="this.Service1"
                  height="250"
                ></v-img>

              </client-only>

            </v-card>
          </v-col>

          <v-col
            class="px-0"
            cols="12"
            md="8"
          >
            <v-card
              flat
              color="transparent"
            >
              <v-card-title>Hot-Dip Coating </v-card-title>

              <v-card-text>
                “Hot-dip galvanizing is a proven technology that combats corrosion for decades without the need for maintenance.” -<a href="https://galvanizeit.org/galvanize-it-online-seminar/structural-steel-reliable-resilient-recyclable">American Galvanizers Association</a> <br>This practice is essentially simple and delivers a definite advantage over other rust protection techniques. As the steel is dipped in the kettle, the iron from the steel metallurgically responds with the molten zinc to create a tightly-bonded metal coating that offers superior rust protection to steel. At North American Galvanizing Industries LLC, we process our work through 5 different preparation pools to allow the steel to bond to the purest zinc coating.
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>

        <v-row
          align="center"
          class="mb-5"
        >
          <v-col
            cols="12"
            md="4"
            order-md="2"
          >
            <v-card outlined>
              <client-only>
                <v-img
                  :src="this.Service2"
                  height="250"
                ></v-img>

              </client-only>

            </v-card>
          </v-col>

          <v-col
            class="px-0"
            cols="12"
            md="8"
          >
            <v-card
              color="transparent"
              flat
            >
              <v-card-title>Efficiency in Delivering
              </v-card-title>

              <v-card-text>
                <p>
                  Our quick turn around times are due to our galvanizing plants high capacity and efficient logistics, when the job needs to get done quickly you can count on us to get it done without compromising quality.

                </p>

              </v-card-text>
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
export default {
  layout: "services",
  metaInfo: {
    title: "Services",
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
    Contact: () => import("@/components/Contact"),
    VideoSheet: () => import("@/components/VideoSheet")
  },

  data: () => ({
    Service1: require("~/assets/Service1.jpg"),
    Service2: require("~/assets/Service2.jpg"),
    testimonial: {
      blurb:
        "With Alpha Construction managing all of our customer-facing services and ASCC, helping us monitor and understand building performance, Abocado is in great shape to create and release new products.",
      person: "Jay Oakrson",
      title: "CEO Avocado"
    },
    features: [
      {
        title: "Quality Tip Galvanizing",
        text:
          "Hot-dip galvanizing is the most effective form of galvanizing which involves the process of coating iron and steel with a molting layer of zinc which protects against corrosion.",
        src: require("~/assets/HotDripGalvanizing.jpg")
      },
      {
        title: "Affordable Expedited Service",
        text:
          "North American Galvanizing Industries LLC has both a 29.6 ft long, 6.7 ft wide and 3.5 ft deep kettle, and a 55.9 ft long , 4 ft wide and 11.6 ft deep kettle; allowing us to supply galvanizing solutions for your most demanding jobs.",
        src: require("~/assets/Columb2.jpg")
      },
      {
        title: "Exceptional Customer Service",
        text:
          "We are based off San Diego County and  can offer solutions in Santa Clarita, Imperial Valley, Riverside, San Bernardino, Orange County, Los Angeles, Ventura and Santa Barbara Counties.",
        src: require("~/assets/Columb3.jpg")
      }
    ]
  })
};
</script>
