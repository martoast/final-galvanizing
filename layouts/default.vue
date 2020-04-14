<template>
  <client-only>
    <v-app dark>

      <AppBar />

      <Hero />

      <!-- <Jumbotron /> -->
      <v-content>

        <v-container>
          <nuxt />
        </v-container>
      </v-content>

      <Footer />
    </v-app>
  </client-only>

</template>

<script>
import Jumbotron from "~/components/Jumbotron.vue";
import AppBar from "~/components/AppBar.vue";
import Footer from "~/components/Footer.vue";
import Hero from "~/components/Hero.vue";

export default {
  components: {
    Jumbotron,
    AppBar,
    Footer,
    Hero
  },
  data() {
    return {
      items: [
        {
          icon: "mdi-apps",
          title: "Welcome",
          to: "/"
        },
        {
          icon: "mdi-chart-bubble",
          title: "Inspire",
          to: "/inspire"
        }
      ]
    };
  }
};
</script>
