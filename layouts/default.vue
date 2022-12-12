<template>
  <v-app class="fontOfTitle">
    <v-app-bar
      class="pt-2"
      style="
        background-color: #1f2024;
        height: 1px;
        border-bottom: 1px solid hsla(0, 0%, 100%, 0.1);
      "
    >
      <v-toolbar-title class="fontOfTitle"
        ><span class="primary--text pr-2">{{ Css }}</span
        >{{ title }}</v-toolbar-title
      >
      <v-spacer />
      <v-hover v-slot="{ hover }" open-delay="200">
        <div
          :elevation="hover ? 1 : 2"
          class="pr-10"
          :class="{ 'primary--text': hover }"
        >
          Selektory CSS
        </div>
      </v-hover>
      <v-hover v-slot="{ hover }" open-delay="200">
        <div
          :elevation="hover ? 16 : 2"
          class="pr-10"
          :class="{ 'primary--text': hover }"
        >
          Właściwości CSS
        </div>
      </v-hover>
      <v-hover v-slot="{ hover }" open-delay="200">
        <div
          class="pr-10"
          :elevation="hover ? 16 : 2"
          :class="{ 'primary--text': hover }"
        >
          Blog
        </div>
      </v-hover>
    </v-app-bar>
    <v-main style="background-color: #1f2024">
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer :absolute="!fixed" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>
<style>
.fontOfTitle {
  font-family: Roboto Mono, monospace;
  font-size: 18px;
}
</style>
<script>
export default {
  name: "DefaultLayout",
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: "mdi-apps",
          title: "Welcome",
          to: "/",
        },
        {
          icon: "mdi-chart-bubble",
          title: "Inspire",
          to: "/inspire",
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "GENERATOR",
      Css: "Css",
    };
  },
};
</script>
