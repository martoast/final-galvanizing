<template>
  <div>
    <div>

      <v-footer
        dark
        height="200px"
        padless
        color="#024283"
      >

        <v-card
          class="flex"
          flat
          tile
          color="#024283"
        >
          <v-row
            justify="space-around"
            align="center"
          >
            <FooterLogo />
            <!-- <h5>Copyright © 2020 Donald Miller Words, LLC. All rights reserved</h5> -->
            <ul class="body-1">
              <v-row>

                <li
                  v-for="(c, i) in company"
                  :key="i"
                >

                  <a
                    class="transition-swing ma-5"
                    v-text="c.title"
                    :href="c.link"
                  />
                </li>
              </v-row>

            </ul>
          </v-row>

        </v-card>

      </v-footer>
    </div>

  </div>
</template>

<script>
import FooterLogo from "~/components/FooterLogo.vue";
export default {
  components: {
    FooterLogo
  },
  data: () => ({
    categories: [
      { title: "SEO Services", link: "/seo" },
      { title: "Web Development", link: "/web-development" },
      { title: "E-Commerce", link: "/ecommerce" },
      { title: "Digital Marketing", link: "/payperclick" }
    ],
    company: [
      { title: "Home", link: "/" },
      { title: "Services", link: "/services" },
      { title: "About", link: "/about" },
      { title: "Contact", link: "/contact" }
    ],
    icons: [
      "mdi-facebook",
      "mdi-twitter",
      "mdi-google-plus",
      "mdi-linkedin",
      "mdi-instagram"
    ],
    details: [
      [
        "mdi-crosshairs-gps",
        "Vía Rápida Oriente 15000",
        "Tijuana, Baja California"
      ],
      ["mdi-email", "", "info@peninsulatijuana.com"],
      ["mdi-phone", "+52 (664) 684 85 40", ""]
    ]
  })
};
</script>

<style lang="sass">
.v-application .v-footer
  ul
    list-style-type: none

    a
      color: white
      text-decoration: none

      &:hover
        color: grey
</style>
