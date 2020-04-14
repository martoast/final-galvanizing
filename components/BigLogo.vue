<template>
  <v-img
    :class="$vuetify.breakpoint.mdAndUp ? 'BigLogo' : 'BigLogo2'"
    alt="Vuetify Logo"
    :src="this.logo"
    to='/'
  >
  </v-img>
</template>

<script>
export default {
  data() {
    return {
      logo: require("~/assets/whitelogo.png")
    };
  },
  mounted() {
    console.log(this.$vuetify.breakpoint);
  },

  computed: {
    imageHeight() {
      switch (this.$vuetify.breakpoint.name) {
        case "xs":
          return "220px";
        case "sm":
          return "400px";
        case "md":
          return "500px";
        case "lg":
          return "600px";
        case "xl":
          return "800px";
      }
    }
  }
};
</script>

<style>
.BigLogo {
  max-width: 1200px;
  max-height: 1000px;
}
.BigLogo2 {
  max-width: 400px;
  max-height: 400px;
}
</style>
