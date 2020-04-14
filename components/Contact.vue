<template>
  <section id="contact" class="py-5">
    <SectionHeader
      header="North American Galvanizing Industries LLC"
      sub-header="Contact us"
      text="Call or submit our online form to request an estimate or for general questions about North American Galvanizing Industries LLC and our services. We look forward to serving you!"
    />

    <v-container>
      <v-row>
        <v-col xs12 md6>
          <v-form>
            <v-container pa-0>
              <v-row>
                <v-col cols="12" md="6">
                  <v-text-field outlined label="First Name*" />
                </v-col>

                <v-col cols="12" md="6">
                  <v-text-field outlined label="Last Name*" />
                </v-col>

                <v-col cols="12" md="6">
                  <v-text-field outlined label="Your Email*" />
                </v-col>

                <v-col cols="12" md="6">
                  <v-text-field label="Your Phone Number*" outlined />
                </v-col>

                <v-col cols="12">
                  <v-text-field label="Subject" outlined />
                </v-col>

                <!-- <v-col cols="12">
                  <v-textarea label="Message" outlined />
                </v-col> -->

                <v-col cols="12">
                  <v-btn
                    :block="$vuetify.breakpoint.xsOnly"
                    color="primary"
                    x-large
                  >
                    Send Message
                  </v-btn>
                </v-col>
              </v-row>
            </v-container>
          </v-form>
        </v-col>

        <v-col cols="12" md="6">
          <v-container fluid pa-0>
            <v-row>
              <v-col cols="12" md="6" class="pa-0">
                <v-card-title>Mailing Address</v-card-title>
                <v-card-text>
                  <div>North American Galvanizing Ind. P.O. Box 121356</div>
                  <div>Chula Vista, CA 91912</div>
                  <div>United States</div>
                </v-card-text>
              </v-col>

              <v-col cols="12" md="6" class="pa-0">
                <v-card-title>Contact Info</v-card-title>
                <v-card-text>
                  <div>+1 (619) 592-9582</div>
                  <div>Fax : +1 (619) 810-0810</div>
                  <div>
                    <a href="#">info@galvanizing-northamerican.com</a>
                  </div>
                </v-card-text>
              </v-col>

              <v-col cols="12">
                <iframe
                  src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d6720.571254558503!2d-117.01872687504873!3d32.625216324072255!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x80d94dfce944ec61%3A0xd297ae31810f003!2sChula%20Vista%2C%20CA%2091912!5e0!3m2!1sen!2sus!4v1586839553120!5m2!1sen!2sus"
                  width="100%"
                  height="400"
                  frameborder="0"
                  style="border:0"
                  allowfullscreen
                />
              </v-col>
            </v-row>
          </v-container>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  metaInfo: {
    title: "Contact",
    meta: [
      {
        name: "description",
        content: "Customized vue-cli templates for Vue and Vuetify"
      }
    ]
  },

  components: {
    Heading: () => import("@/components/Heading"),
    SectionHeader: () => import("@/components/SectionHeader")
  }
};
</script>
