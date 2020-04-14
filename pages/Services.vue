<template>
  <div>
    <section
      id="services"
      class="py-5"
    >
      <SectionHeader
        header="North American Galvanizing Industries LLC"
        sub-header="Explore our Services"
      />

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
              <v-img
                :src="this.Service1"
                height="250"
              />
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
                “Hot-dip galvanizing is a proven technology that combats corrosion for decades without the need for maintenance.”-American Galvanizers Association (Lets backlink to their website) This practice is essentially simple and delivers a definite advantage over other rust protection techniques. As the steel is dipped in the kettle, the iron from the steel metallurgically responds with the molten zinc to create a tightly-bonded metal coating that offers superior rust protection to steel. At North American Galvanizing Industries LLC, we process our work through 5 different preparation pools to allow the steel to bond to the purest zinc coating.
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
              <v-img
                :src="this.Service2"
                height="250"
              />
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
                  Our quick Turn around times are due to our galvanizing plants high capacity and efficient logistics, when the job needs to get done quickly you can count on us to get it done without compromising quality.

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
    Service1: require("@/assets/Service1.jpg"),
    Service2: require("@/assets/Service2.jpg"),
    testimonial: {
      blurb:
        "With Alpha Construction managing all of our customer-facing services and ASCC, helping us monitor and understand building performance, Abocado is in great shape to create and release new products.",
      person: "Jay Oakrson",
      title: "CEO Avocado"
    }
  })
};
</script>
