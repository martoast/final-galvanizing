<template>
  <div>
    <client-only>
      <v-img
        v-if="namespace"
        :src="this.src"
        aspect-ratio="4.0"
        height="100vh"
      >
      </v-img>
    </client-only>

  </div>

</template>

<script>
import BigLogo from "~/components/BigLogo.vue";
export default {
  data: () => ({
    src: require("~/assets/About.jpg")
  }),
  components: { BigLogo },

  computed: {
    namespace() {
      return this.$route.name;
    }
  }
};
</script>
