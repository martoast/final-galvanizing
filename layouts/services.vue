<template>
  <v-app dark>

    <Appbar2 />

    <!-- <Jumbotron /> -->
    <v-content>

      <v-container>
        <nuxt />
      </v-container>
    </v-content>

  </v-app>
</template>

<script>
import Jumbotron from "~/components/Jumbotron.vue";
import Appbar2 from "~/components/Appbar2.vue";
import Footer from "~/components/Footer.vue";
import Hero from "~/components/Hero.vue";

export default {
  components: {
    Jumbotron,
    Appbar2,
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
