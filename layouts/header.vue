<template>
  <v-app-bar
    app
    elevate-on-scroll
    color="transparent"
    height="100px"
    class="col-lg-12 mx-auto"
    hide-on-scroll
  >
    <v-app-bar-nav-icon v-show="$vuetify.breakpoint.mobile" />
    <v-img
      :src="logo"
      alt="logo"
      class="ma-4"
      contain
      height="40"
      max-width="136"
    ></v-img>
    <v-spacer v-show="!$vuetify.breakpoint.mobile"></v-spacer>
    <v-row v-show="!$vuetify.breakpoint.mobile">
      <v-btn
        v-for="link in links"
        :key="link.text"
        justify="center"
        align="center"
        :to="link.path"
        text
        class="text-capitalize white--text"
        >{{ link.text }}</v-btn
      >
    </v-row>
    <v-spacer v-show="!$vuetify.breakpoint.mobile"></v-spacer>
    <v-btn rounded large color="primary" class="text-capitalize">{{
      callText
    }}</v-btn>
  </v-app-bar>
</template>

<script>
export default {
  data() {
    return {
      logo: require("@/assets/img/logo.svg"),
      callText: "Call Us",
      links: [
        {
          text: "Home",
          path: "/",
        },
        {
          text: "About",
          path: "/about",
        },
        {
          text: "Hotel",
          path: "/hotel",
        },
        {
          text: "Bar & Restaurant",
          path: "/bar",
        },
        {
          text: "Guest House",
          path: "/guest-house",
        },
      ],
    };
  },
};
</script>
