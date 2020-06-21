<template>
  <div>
    <StartScreen
      pageHeading="DEGREES"
      caption="Lorem ipsum dolor sit amet, consectetur adipiscing elit phasellus trist."
    />
    <v-row
      v-for="degree in degreeDetails"
      :key="degree.subject"
      class="screen2"
    >
      <v-col class="order-1" cols="1"></v-col>
      <v-col class="order-3" cols="12" sm="12" md="5">
        <v-btn class="mb-5 ml-5" color="warning">{{ degree.cost }}</v-btn>
        <h3 class="mb-5 ml-5">{{ degree.subject }}</h3>
        <p class="ml-5">{{ degree.content }}</p>
      </v-col>
      <v-col
        v-if="$vuetify.breakpoint.mdAndUp && degree.id % 2 === 0"
        class="order-3"
        cols="12"
        sm="12"
        md="5"
      >
        <v-img :src="degree.image"></v-img>
        <!-- <img :src="degree.image" /> -->
      </v-col>
      <v-col v-else class="order-2" cols="12" sm="12" md="5">
        <v-img :src="degree.image"></v-img>
        <!-- <img :src="degree.image" /> -->
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
    degreeDetails: [
      {
        id: 1,
        image: require("../assets/degree-1.jpg"),
        cost: "$21,500",
        subject: "COMPUTER SCIENCE",
        content:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus eumauris eleifend, rhoncus metus vel, vestibulum odio. Suspendisse egetante vel arcu pretium eleifend vel quis dolor. In aliquam, elit quis lacinia ornare, nunc mauris aliquam erat, scelerisque laoreet nunclectus ut dui."
      },
      {
        id: 2,
        image: require("../assets/degree-2.jpg"),
        cost: "$11,300",
        subject: "LIBERAL ARTS",
        content:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus eumauris eleifend, rhoncus metus vel, vestibulum odio. Suspendisse egetante vel arcu pretium eleifend vel quis dolor. In aliquam, elit quislacinia ornare, nunc mauris aliquam erat, scelerisque laoreet nunclectus utd."
      },
      {
        id: 3,
        image: require("../assets/degree-3.jpg"),
        cost: "$21,900",
        subject: "HUMANITIES",
        content:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus eumauris eleifend, rhoncus metus vel, vestibulum odio. Suspendisse egetante vel arcu pretium eleifend vel quis dolor. In aliquam, elit quis lacinia ornare, nunc mauris aliquam erat, scelerisque laoreet nunclectus ut dui."
      },
      {
        id: 4,
        image: require("../assets/degree-4.jpg"),
        cost: "$34,000",
        subject: "APPLIED SCIENCE",
        content:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus eumauris eleifend, rhoncus metus vel, vestibulum odio. Suspendisse egetante vel arcu pretium eleifend vel quis dolor. In aliquam, elit quislacinia ornare, nunc mauris aliquam erat, scelerisque laoreet nunclectus utd."
      }
    ]
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
