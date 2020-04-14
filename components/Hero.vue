<template>
  <div>
    <client-only>
      <v-img
        v-if="namespace"
        :src="this.src"
        aspect-ratio="4.0"
        height="100vh"
      >
        <div>
          <HeroFlex />
        </div>

      </v-img>
    </client-only>

  </div>

</template>

<script>
import HeroFlex from "~/components/HeroFlex.vue";
import BigLogo from "~/components/BigLogo.vue";
export default {
  data: () => ({
    src: require("~/assets/finalhero.jpg")
  }),
  components: { BigLogo, HeroFlex },

  computed: {
    namespace() {
      return this.$route.name;
    }
  }
};
</script>
