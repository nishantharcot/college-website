<template>
  <div>
    <StartScreen
      pageHeading="DEGREES"
      caption="Lorem ipsum dolor sit amet, consectetur adipiscing elit phasellus trist."
    />
    <v-row class="screen2">
      <v-col cols="1"></v-col>
      <v-col cols="12" sm="12" md="5">
        <v-img src="../assets/degree-1.jpg"></v-img>
      </v-col>
      <v-col cols="12" sm="12" md="5">
        <v-btn class="mb-5 ml-5" color="warning">$21,500</v-btn>
        <h3 class="mb-5 ml-5">COMPUTER SCIENCE</h3>
        <p class="ml-5">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus eu
          mauris eleifend, rhoncus metus vel, vestibulum odio. Suspendisse eget
          ante vel arcu pretium eleifend vel quis dolor. In aliquam, elit quis
          lacinia ornare, nunc mauris aliquam erat, scelerisque laoreet nunc
          lectus ut dui.
        </p>
      </v-col>
      <v-col cols="1"></v-col>
    </v-row>
    <v-row class="screen2">
      <v-col class="order-1" cols="1"></v-col>
      <v-col class="order-3" cols="12" sm="12" md="5">
        <v-btn class="mb-5 ml-5" color="warning">$11,300</v-btn>
        <h3 class="mb-5 ml-5">LIBERAL ARTS</h3>
        <p class="ml-5">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus eu
          mauris eleifend, rhoncus metus vel, vestibulum odio. Suspendisse eget
          ante vel arcu pretium eleifend vel quis dolor. In aliquam, elit quis
          lacinia ornare, nunc mauris aliquam erat, scelerisque laoreet nunc
          lectus utd.
        </p>
      </v-col>
      <v-col
        v-if="$vuetify.breakpoint.mdAndUp"
        class="order-3"
        cols="12"
        sm="12"
        md="5"
      >
        <v-img src="../assets/degree-2.jpg"></v-img>
      </v-col>
      <v-col v-else class="order-2" cols="12" sm="12" md="5">
        <v-img src="../assets/degree-2.jpg"></v-img>
      </v-col>
      <v-col class="order-4" cols="1"></v-col>
    </v-row>
    <v-row class="screen2">
      <v-col cols="1"></v-col>
      <v-col cols="12" sm="12" md="5">
        <v-img src="../assets/degree-3.jpg"></v-img>
      </v-col>
      <v-col cols="12" sm="12" md="5">
        <v-btn class="mb-5 ml-5" color="warning">$21,900</v-btn>
        <h3 class="mb-5 ml-5">HUMANITIES</h3>
        <p class="ml-5">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus eu
          mauris eleifend, rhoncus metus vel, vestibulum odio. Suspendisse eget
          ante vel arcu pretium eleifend vel quis dolor. In aliquam, elit quis
          lacinia ornare, nunc mauris aliquam erat, scelerisque laoreet nunc
          lectus ut dui.
        </p>
      </v-col>
      <v-col cols="1"></v-col>
    </v-row>
    <v-row class="screen2">
      <v-col class="order-1" cols="1"></v-col>
      <v-col class="order-3" cols="12" sm="12" md="5">
        <v-btn class="mb-5 ml-5" color="warning">$34,000</v-btn>
        <h3 class="mb-5 ml-5">APPLIED SCIENCE</h3>
        <p class="ml-5">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus eu
          mauris eleifend, rhoncus metus vel, vestibulum odio. Suspendisse eget
          ante vel arcu pretium eleifend vel quis dolor. In aliquam, elit quis
          lacinia ornare, nunc mauris aliquam erat, scelerisque laoreet nunc
          lectus utd.
        </p>
      </v-col>
      <v-col
        v-if="$vuetify.breakpoint.mdAndUp"
        class="order-3"
        cols="12"
        sm="12"
        md="5"
      >
        <v-img src="../assets/degree-4.jpg"></v-img>
      </v-col>
      <v-col v-else class="order-2" cols="12" sm="12" md="5">
        <v-img src="../assets/degree-4.jpg"></v-img>
      </v-col>
      <v-col class="order-4" cols="1"></v-col>
    </v-row>
    <CollegeStats />
    <v-row id="screen3" app>
      <v-col cols="1"></v-col>
      <v-col class="centerClass" cols="10">
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus eu
          mauris eleifend, rhoncus metus vel, vestibulum odio. Suspendisse eget
          ante vel arcu pretium eleifend vel quis dolor. In aliquam, elit quis
          lacinia ornare, nunc mauris aliquam erat, scelerisque laoreet nunc
          lectus utd.
        </p>
        <v-btn x-large color="warning" class="mt-5">
          <v-icon class="mr-3">fas fa-graduation-cap</v-icon>ENROLL TODAY
        </v-btn>
      </v-col>
      <v-col cols="1"></v-col>
    </v-row>
  </div>
</template>

<script>
import CollegeStats from "@/components/CollegeStats.vue";
import StartScreen from "@/components/StartScreen.vue";
export default {
  data: () => ({
    //
  }),
  components: {
    CollegeStats,
    StartScreen
  }
};
</script>

<style lang="scss" scoped>
h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: "Roboto Slab", serif !important;
}
#screen1 {
  background-image: url("../assets/gallery.jpg");
}

.screen2 {
  min-height: 65vh;
  display: flex;
  justify-content: space-around;
  align-items: center;
}

#screen3 {
  min-height: 30vh;
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.centerClass {
  text-align: center;
}
</style>
