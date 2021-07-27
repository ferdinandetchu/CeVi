<template>
  <v-row justify="center" align="center">
    <v-col cols="7">
      <v-img class="welcome-imag" src="/graphic-designer-tools-icon-pattern-background-vector.jpg"></v-img>
    </v-col>
    <v-col cols="5">
      <h1 class="primary--text py-0 my-0">
        Welcome to CeVi
      </h1>
      <p class="mt-0 pt-0 primary--text"><i>we are her for you</i></p>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
        quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
        consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
        cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
        proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
      </p>
      <v-btn class="text-capitalize" large color="primary">Get Started</v-btn>
    </v-col>
    <v-col cols="12">
       <v-img class="background-picture" src="/graphic-designer-tools-icon-pattern-background-vector.jpg">
         <v-row style="background-color: rgba(21, 101, 192,0.5);" class="justify-center align-center fill-height">
          <h1 class="white--text display-2 font-weight-bold">
            Conect With Love Once
          </h1>
         </v-row>
       </v-img>
    </v-col>
    <v-col cols="12">
      <h1 class="primary--text">Available categories</h1>
      <v-sheet
        class="mx-auto"
      >
        <v-slide-group
          v-model="model"
          class="pa-4"
          show-arrows
        >
          <v-slide-item
            v-for="n in 15"
            :key="n"
            v-slot="{ active, toggle }"
          >
            <v-card
              :color="active ? 'primary' : 'grey lighten-1'"
              class="ma-4"
              height="200"
              width="100"
              @click="toggle"
            >
              <v-img class="fill-height" src="/photo-1512295767273-ac109ac3acfa.jpeg">
                <v-row
                  class="fill-height"
                  align="center"
                  justify="center"
                >
                  <v-col cols="12">
                      <v-row
                        justify="center"
                      >
                      <v-scale-transition>
                        <v-icon
                          v-if="active"
                          color="primary"
                          size="48"
                          v-text="'mdi-close-circle-outline'"
                        ></v-icon>
                      </v-scale-transition>
                    </v-row>
                    <h3 style="text-align: center;" class="primary--text">
                      Birthday
                    </h3>
                  </v-col>
                </v-row>
              </v-img>
            </v-card>
          </v-slide-item>
        </v-slide-group>

        <v-expand-transition>
          <v-sheet
            v-if="model != null"
            height="200"
            tile
          >
            <v-row>
              <v-col cols="12">
                <h4 class="primary--text big-divider">Templates</h4>
              </v-col>
              <v-col
                v-for="n in 9"
                :key="n"
                class="d-flex child-flex"
                cols="4"
              >
                <v-img
                  :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
                  :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
                  aspect-ratio="1"
                  class="grey lighten-2"
                >
                  <template v-slot:placeholder>
                    <v-row
                      class="fill-height ma-0"
                      align="center"
                      justify="center"
                    >
                      <v-progress-circular
                        indeterminate
                        color="grey lighten-5"
                      ></v-progress-circular>
                    </v-row>
                  </template>
                </v-img>
              </v-col>
            </v-row>
          </v-sheet>
        </v-expand-transition>
      </v-sheet>
    </v-col>
  </v-row>
</template>

<script>

  export default {
    data: () => ({
      model: null,
    }),
  };
</script>

<style lang="css" scoped>
.welcome-imag {
  /*height: 100vh; */
  clip-path: polygon(25% 0%, 100% 0%, 75% 100%, 0% 100%);
  border-color: #1565C0;
  border-width: 20px;
  border-style: solid;
}
.background-picture{
  clip-path: circle(35% at 50% 50%);
}
.big-divider {
  border-left: solid 3px #1565C0;
  border-bottom: solid 3px #1565C0;
  width: 30px;
  padding-left: 5px;
}
</style>
