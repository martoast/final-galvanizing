<template>
  <section
    id="contact"
    class="py-5"
  >
    <Contact />
  </section>
</template>

<script>
export default {
  layout: "services",
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
    Contact: () => import("@/components/Contact")
  }
};
</script>
