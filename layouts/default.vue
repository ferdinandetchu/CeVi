<template>
  <v-app dark>
    
    <v-app-bar
      app
      color="primary"
      dark
      shrink-on-scroll
      prominent
      src="/top-view-graphic-designer-table-260nw-739911724.webp"
      fade-img-on-scroll
      scroll-target="#scrolling-techniques-5"
      scroll-threshold="500"
    >
      <template v-slot:img="{ props }">
        <v-img
          v-bind="props"
          gradient="to top right, rgba(25, 118, 210,.4), rgba(21, 101, 192,.7)"
        ></v-img>
      </template>

      <v-app-bar-nav-icon class="hidden-md-and-up"></v-app-bar-nav-icon>

      <v-app-bar-title><nuxt-link style="color: white; text-decoration: none;" to="/">CeVi</nuxt-link></v-app-bar-title>

      <v-spacer></v-spacer>
      <v-btn to="/auth/register" color="primary" class="mx-5" fab large>
        Register
      </v-btn>
      <v-btn to="/auth/login" color="white" class="primary--text" fab large>
        Login
      </v-btn>
      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-app-bar>
    <v-sheet
      id="scrolling-techniques-5"
      class="overflow-y-auto"
      max-height="100vh"
    >
      <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    </v-sheet>
    
    
    <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      fixed: false,
    }
  }
}
</script>
