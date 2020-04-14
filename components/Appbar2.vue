<template>
  <div>
    <v-app-bar
      v-scroll="onScroll"
      color="rgba(66, 66, 66)"
      :hide-on-scroll="$vuetify.breakpoint.smAndDown"
      app
      elevate-on-scroll
      dark
    >
      <VuetifyLogo />
      <v-spacer />
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn
          v-for="(item, i) in items"
          :key="i"
          :active-class="!isScrolling ? 'primary--text' : undefined"
          :to="item.to"
          text
        >
          <span v-text="item.text" />
        </v-btn>
      </v-toolbar-items>

      <v-icon @click.stop="drawer = !drawer" class="hidden-md-and-up"
        >mdi-menu</v-icon
      >
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" :right="right" temporary fixed>
      <v-list>
        <v-list-item v-for="(item, i) in items" :key="i" :to="item.to" link>
          <v-list-item-content>
            <v-list-item-title>{{ item.text }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
// Utilities
import { mapMutations } from "vuex";
import VuetifyLogo from "~/components/VuetifyLogo.vue";

export default {
  components: {
    VuetifyLogo
  },
  data: () => ({
    isScrolling: false,
    clipped: false,
    drawer: false,
    fixed: false,
    miniVariant: false,
    right: true,
    rightDrawer: false,
    title: "Vuetify.js",
    Menuitems: [
      { title: "Services", icon: "dashboard" },
      { title: "Projects", icon: "account_box" },
      { title: "Contact", icon: "gavel" }
    ]
  }),

  computed: {
    items() {
      return [
        {
          to: "/",
          text: "Home"
        },
        {
          to: "/services",
          text: "Services"
        },
        {
          to: "/about",
          text: "About"
        },
        {
          to: "/contact",
          text: "Contact"
        }
      ];
    }
  },

  methods: {
    ...mapMutations(["toggleDrawer"]),
    onScroll() {
      this.isScrolling =
        (window.pageYOffset || document.documentElement.scrollTop || 0) > 25;
    }
  }
};
</script>
