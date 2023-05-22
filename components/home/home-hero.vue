<template>
  <div id="home-hero">
    <v-carousel
      cycle
      continuous
      hide-delimiter-background
      height="100vh"
    >
      <v-carousel-item v-for="(slide, i) in slides" :key="i" :src="slide.img">
        <v-row class="fill-height" align="center"  justify="center">
          <v-col cols="6" class="mx-auto">
            <h1 class="text-center white--text">{{ slide.title }}</h1>
            <p class="text-center white--text">{{ slide.description }}</p>
            <v-row justify="center">
              <v-btn
                rounded
                small
                color="primary"
                :to="slide.path"
                class="text-capitalize"
                >{{ slide.cta }}</v-btn
              >
            </v-row>
          </v-col>
        </v-row>
      </v-carousel-item>
    </v-carousel>
  </div>
</template>

<script>
export default {
  data() {
    return {
      slides: [
        {
            title: "Lorem Ipsun Dolor Sit",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
          cta: "Check Our Menu",
          path: "/about",
          img: require("@/assets/img/home/menu-slide.png"),
        },
        {
          title: "Lorem Ipsun Dolor Sit",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
          cta: "Check Our Menu",
          path: "/about",
          img: require("@/assets/img/home/menu-slide.png"),
        },
        {
          title: "Lorem Ipsun Dolor Sit",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
          cta: "Check Our Menu",
          path: "/about",
          img: require("@/assets/img/home/menu-slide.png"),
        },
      ],
    };
  },
};
</script>

<style scoped>
</style>